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

Inside the "Group Role – Edit Members" interface, the DXC Knowledge Authors role is assigned to the group by selecting it from the searchable list and adding it to the Roles List.
  ![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Group%20Role%20Edit%20Members.png?raw=true)

---
Now we will manually create the Knowledge Base:
All > Knowledge > Administration > Knowledge Bases <br>

Once we get to the List of Knowledge Bases, we click New <br>

Publish workflow (the process in which the article needs to get approved to actually show up on the knowledge base We will work with whats already loaded, the Knowledge - Instant Publish <br>
After we save, we see that now we have USer Critirea tabs like Can Read, Can Contribute, and Knowledge Categories <br>
Note: the Knowledge Category, even though we have one knowledge base, we can still split it up to different categories
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Knowledge%20Base.png?raw=true)
We'll create one category: Data Issues
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Knowledge%20Category%20-%20Data%20Issues.png?raw=true)
Inside the Can Read tab, we will click New to create a new user criteria record
- for them to be able to read it, they need to have that specific role (DXC_employee)
  ![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/User%20Criteria%20New%20Record.png?raw=true)
Next, we'll edit the Can Contribute tab - where they can read and edit.
In this new Record, we have a few options. We have the option to add the Role we created for who can contribute and the group as well. So now its saying that if its part of the group or if it has that specific role. We will pick both and then select the Match All box which mean you have to be both part of the group and the specific role to be able to contribute to the specific knowledge base. 
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/User%20Criteria%20Can%20Contribute.png?raw=true)

There are different ways that we could go ahead and combine it, though we could just make it so that only part of that group is required.
And then we could give, read use or give that specific group the employee role, Since the role already exists for reading and that role kind of highlights being an employee for the company. Or we can just add anothe Can read criteria <br>
We will give one more Can Read permission. We will add DXC KB Authors to Roles as well for Can Read.<br>
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/DXC%20KB%20Authors%20Can%20Read%20User%20Criteria.png?raw=true)

We will view the Knowledge Base
All > Service Deck > Knowledge <br>
We can see the new knowldege base has been created
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Home%20Knowledge%20.png?raw=true)

There are no articles in the DXC Tech IT Support KB
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/DXC%20Tech%20IT%20Support%20KB.png?raw=true)
To bring in articles:
All > Knowledge > Articles(Module) > Create New *OR* Import Articles

Once we go ahead and upload that article, it's going to get saved as a draft in the system. Since we chose the approval process to be instant. Once it gets published, it automatically gets added to our knowledge base.
- Selet the appropriate knowledge base created : DXC Tech IT Support KB <br>
- Select the category : Data Issues
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Import%20Article.png?raw=true)
- After we click continue, it gives us the record number to click on for a preview of what the article would look like
  ![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Preview%20of%20Article.png?raw=true)

All > Knowledge > Articles > All <br>
We'll open the record and click Publish
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Publish%20Knowledge%20Record.png?raw=true)




  


