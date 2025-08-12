# August-7-ServiceNow-Knowledge-Management

**Activity Scenario**:
Over the past few months, your team has been resolving more internal support issues than ever (device provisioning, VPN access, software installs) but all of the documentation is scattered across emails, chat threads, and outdated shared folders. <br>

Leadership has now decided it's time to centralize this knowledge into an official IT Support Knowledge Base inside ServiceNow. <br>

But they've made one thing clear: <br>
>"If we're going to do this, it needs to be locked down from day one. We only want trusted people seeing and contributing to this KB."

Your task:

- **Create a Custom Contributor Role** <br>
    - Name: Knowledge_Authors
- **Create a Group and Assign the Role** <br>
    - Name: Knowledge_Authors
- **Create the Knowledge Base**
    - Name: DXC Tech IT Support KB
- **Create User Criteria**
    - Can Read: DXC_KB_Read_Access
    - Can Contribute: DXC_KB_Contribute_Access
- **Test Access**

---

**First, create a role and a group**
We're goning to do 2 different things:
-A user which can go ahead and go into our knowledge base and just read articles right? They'll have the ability to use it, 
-An author which is gonna be able to view it and make edits to it.

The combinations are endless in this specific case but 
- We are going to create one group and one role and reuse a role we have in the system which is DXC EMployee( If you are an Employee you should have acess to the knowledge base. Only if you're an author, then you have the ability to view it and edit. (we will create this)
  ![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/DXC%20Knowledge%20Authors%20Group.png?raw=true)

  To create role:
  All > Roles
  ![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/DXC%20Knowledge%20Authors%20Role.png?raw=true)

  We now created a Group and Role, now we will add the role to the group we just created, and in the Roles tab, we will click Edit <br>
  ![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Edit%20Roles%20tab%20in%20the%20Authors%20Group%20.png?raw=true)


