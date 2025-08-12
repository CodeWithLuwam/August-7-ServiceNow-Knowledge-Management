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
