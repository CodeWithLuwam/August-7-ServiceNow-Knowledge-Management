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
### 1. Create the Custom Role
- Navigate to: All > Roles
- Click **New** and create the role: <br>
    - **Name**: `Knowledge_Authors`
- Save the role. <br>
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/DXC%20Knowledge%20Authors%20Role.png?raw=true)

---
### 2. Create the Group and Assign the Role
- Go to: **All > User Administration > Groups**
- Click **New** and create the group:
    - Name: `Knowledge_Authors`
- Save the group. <br>
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/DXC%20Knowledge%20Authors%20Group.png?raw=true)
- Open the **Roles** tab in the group record.
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Edit%20Roles%20tab%20in%20the%20Authors%20Group%20.png?raw=true)
- Click **Edit** and add the **Knowledge_Authors** role from the searchable list.
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Group%20Role%20Edit%20Members.png?raw=true)
  
---

### 3. Create the Knowledge Base
- Navigate to: **All > Knowledge > Administration > Knowledge Bases**
- Click **New** and create the KB:
    - **Name**: `DXC Tech IT Support KB`
    - **Publish Workflow**: `Knowledge - Instant Publish`
- Save the KB.
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Knowledge%20Base.png?raw=true)

---

### 4. Create Knowledge Categories
- After saving, open the KB record and go to the **Knowledge Categories** tab.
- Click **New** and create:
    - **Name**: Data Issues <br>
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Knowledge%20Category%20-%20Data%20Issues.png?raw=true)


Note: the Knowledge Category, even though we have one knowledge base, we can still split it up to different categories

---

### 5. Configure Read & Contribute Access
**Read Access** <br>
- Go to the **Can Read** tab in the KB record. <br>
- Click **New**:<br>
    - **Name**: `DXC Employee`
    - Add **DXC_employee** role.
 ![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/User%20Criteria%20New%20Record.png?raw=true)
- Save. <br>

**Contribute Access** <br>
- Go to the **Can Contribute** tab.
- Click **New**: <br>
    - **Name**: `DXC KB Authors` <br>
    - Add **DXC Knowledge Authors** role and **DXC Knowledge Authors** group. <br>
    - Select **Match All** (must be in the group and have the role). <br>
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/User%20Criteria%20Can%20Contribute.png?raw=true)
- Save.

---

### 6. Add Articles
- Navigate to: **All > Knowledge > Articles**
- Click **Create New** (or **Import Articles**).
- Select: <br>
  - **Knowledge Base**: `DXC Tech IT Support KB`
  - **Category**:` Data Issues`
- Save as draft.
- Click **Publish** (Instant Publish will make it live immediately).

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

---
### 7. Test Access
- Go to **All > Service Deck > Knowledge** <br>
- Select **DXC Tech IT Support KB** <br>
- Confirm: <br>
    - Employees with `DXC_employee` role can read.
    - Members of `Knowledge_Authors` group with the `Knowledge_Authors` role can **read and contribute**. <br>
- Verify articles appear and permissions work as expected.
And we see the article <br>
![](https://github.com/CodeWithLuwam/August-7-ServiceNow-Knowledge-Management/blob/main/Images/Published%20Article.png?raw=true)




  


