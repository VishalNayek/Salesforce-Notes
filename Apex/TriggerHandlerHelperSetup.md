# Apex Triggers

## What is a Trigger?

A trigger is Apex code that executes before or after DML events.

## Trigger Events

- before insert
- before update
- before delete
- after insert
- after update
- after delete
- after undelete

## Best Practices

- One trigger per object
- Use Trigger Handler
- Bulkify code
- Avoid SOQL in loops

## Setup Trigger, TriggerHandler, TriggebeforeInsertrHelper - Best Practice

### AccountTrigger

```apex
trigger AccountTrigger on Account (beforeInsert, beforeUpdate, beforeDelete, afterInsert, afterUpdate, afterDelete, afterUndelete){
    AccountTriggerHandler handler = new AccountTriggerHandler();
    if(Trigger.isBefore){
        if(Trigger.isInsert) handler.beforeInsert();
        if(Trigger.isUpdate) handler.beforeUpdate();
        if(Trigger.isDelete) handler.beforeDelete();
    }
    if(Trigger.isAfter){
        if(Trigger.isInsert) handler.afterInsert();
        if(Trigger.isUpdate) handler.afterUpdate();
        if(Trigger.isDelete) handler.afterDelete();
        if(Trigger.isUndelete) handler.afterUndelete();
    }
}
```
### AccountTriggerHandler

```apex
public without sharing class AccountTrigger{
    private List<Accounts> newRecords;
    private List<Accounts> oldRecords;
    private Map<Id, Account> newMap;
    private Map<Id, Account> oldMap;

    //initialise the values with constructor
    public AccountTriggerHandler(){
        this.newRecords = (List<Account>) Trigger.new;
        this.oldRecords = (List<Account>) Trigger.old;
        this.newMap = (Set<Id, Account>) Trigger.newMap;
        this.oldMap = (Set<Id, Account>) Trigger.oldMap;
    }

    //Trigger.old and Trigger.oldMap is only available on update and delete (both before and after)

    public void beforeInsert(){

    }

    public void beforeUpdate(){

    }

    public void beforeDelete(){

    }

    public void afterInsert(){

        List<Account> accList = new List<Account>();

        for(Account acc: newRecords){
            if (acc.description==null){
               accList.add(acc);
            }
        }

        AccountTriggerHandler.populateDescription(accList);

    }

    public void afterUpdate(){

    }

    public void afterDelete(){

    }

    public void afterUndelete(){

    }

}
```

### AccountTriggerHelper

```apex
public without sharing class AccountTriggerHelper{

    public static void populateDescription(List<Account> accList){
        List<Account> accToUpdate = new List<Account>();
        for(Account acc : accList){
            acc.description = 'Updated from Trigger';
            accToUpdate.add(acc);
        }

        Database.Update(accToUpdate);
    }
}
```

