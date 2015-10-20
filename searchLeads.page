<apex:page controller="theController">
   <apex:form>
      <apex:pageBlock mode="edit" id="block">
         <apex:pageBlockSection>
            <apex:pageBlockSectionItem>
               <apex:outputLabel for="searchText">Search Text</apex:outputLabel>
               <apex:panelGroup>
                  <apex:inputText id="searchText" value="{!searchText}"/>
                  <apex:commandButton value="Go!" action="{!doSearch}" 
                                      rerender="block" status="status"/>
               </apex:panelGroup>
            </apex:pageBlockSectionItem>
        </apex:pageBlockSection>
        <apex:actionStatus id="status" startText="requesting..."/>
        <apex:pageBlockSection title="Results" id="results" columns="1">
           <apex:pageBlockTable value="{!results}" var="l" 
                               rendered="{!NOT(ISNULL(results))}">
              <apex:column value="{!l.name}"/>
              <apex:column value="{!l.email}"/>
              <apex:column value="{!l.phone}"/>
           </apex:pageBlockTable>
        </apex:pageBlockSection>
      </apex:pageBlock>
   </apex:form>
</apex:page>
