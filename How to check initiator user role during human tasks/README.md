**Implementation details**

This implementation shows how to implement the use case described in the question: [How to check initiator user role during human tasks](https://community.bonitasoft.com/questions-and-answers/how-check-initiator-user-role-during-human-tasks)

It has been implemented with Bonita 7.10.3 Community Edition:

Actor Filter Definiton:  
role-escalation: takes the name of the step and the process instance ID to look at.  

Actor Filter Implementation:  
<pre><code>
List<UserMembership> listOfUserMemberships = getAPIAccessor().getIdentityAPI().getUserMemberships(task.getExecutedBy(), 0, 100, UserMembershipCriterion.GROUP_NAME_ASC);  
List<UserMembership> taskPerformerRole = listOfUserMemberships.stream().filter(m -> (CUSTOMER_MANAGER_ROLE_NAME.equalsIgnoreCase(m.getRoleName()) || SALES_MANAGER_ROLE_NAME.equalsIgnoreCase(m.getRoleName()))).collect(Collectors.toList());  

</code></pre>

