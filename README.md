# Visualforce

## Standard Controller

## Custom Controller

## Standard List Controller

Standard List Controller - To create Visualforce pages that can display or act on a set of records.  The standard list controller provides many powerful, automatic behaviors such as querying for records of a specific object and making the records available in a collection variable, as well as filtering of and pagination through the results. Adding the standard list controller to a page is very similar to adding the standard (record) controller, but with the intent of working with many records at once, instead of one record at a time.

### Display a List of Records

Use the standard list controller and an iteration component, such as `<apex:pageBlockTable>`, to display a list of records.  The standard (record) controller makes it easy to get a single record loaded into a variable you can use on a Visualforce page. The standard list controller is similar, except instead of a single record, it loads a list, or collection, of records into the variable.

Because you’re dealing with a collection, instead of an individual record, you need to use an iteration component to display them. An iteration component works with a collection of similar items, instead of on a single value. An iteration component loops through its collection, and for each record, generates some output based on a template you provide as part of the component markup.

ContactList.vfp
``` Apex
<apex:page standardController="Contact" recordSetVar="contacts">
    <apex:pageBlock title="Contacts List">
    
      <!-- Contacts List -->
      <apex:pageBlockTable value="{! contacts}" var="ct">
            <apex:column value="{! ct.FirstName }"/>
            <apex:column value="{! ct.LastName }"/>
            <apex:column value="{! ct.Email }"/>
            <apex:column value="{! ct.Account.Name }"/>
      </apex:pageBlockTable>
      
    </apex:pageBlock>
</apex:page>
```      
