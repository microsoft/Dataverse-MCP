# 🧑🏽‍💻 Lab 03 - Use the Dataverse MCP server with Visual Studio Code

In Visual Studio Code, open GitHub Copilot by selecting the **GitHub Copilot icon** or use **ctrl+alt+I**.

Change GitHub Copilot from ask mode to agent mode.

![Change from ask to agent mode](./assets/change-ask-agent-mode.png)

Make sure to refresh the tools to make sure the Dataverse MCP server details get loaded from the Claude configuration.

![Refresh tools](./assets/refresh-tools.png)

Now you can select the tools icon to open the available tools.

![Select tools](./assets/select-tools.png)

Depending on your extensions, the list can differ, but the `Dataverse MCP Server` should be listed with a text `from Claude Desktop`.

![Available tools](./assets/available-tools.png)

Make sure the tools are selected, and select `OK`.

Let's start by asking again about the tables in Dataverse:

```
List tables from Dataverse
```

GitHub Copilot will ask you if you want to continue running the `list_tables` tool. 

![Confirm list_tables tool run](./assets/confirm-tool-run.png)

Select `Continue` and you should see something like the following response:

![List_tables tool response](./assets/list-tables-response.png)

Now, let's list the items in the contact table again by running the following prompt:

```
List items in the contact table
```

Select `Continue` to run the tools needed. It will return items, but it might not return all the items in the table. If that happens, make sure to ask for 10 items. That should return all 10 items.

```
Here are 10 records from the contact table:

John (sample) Smith
Email: john.smith@example.com
Job Title: Marketing Manager
Phone: 555-123-4567

Sarah (sample) Johnson
Email: sarah.johnson@example.com
Job Title: Sales Director
Phone: 555-234-5678

Michael (sample) Brown
Email: michael.brown@example.com
Job Title: IT Manager
Phone: 555-345-6789

Emily (sample) Davis
Email: emily.davis@example.com
Job Title: HR Specialist
Phone: 555-456-7890

David (sample) Wilson
Email: david.wilson@example.com
Job Title: Finance Director
Phone: 555-567-8901

Jessica (sample) Martinez
Email: jessica.martinez@example.com
Job Title: Product Manager
Phone: 555-678-9012

Robert (sample) Taylor
Email: robert.taylor@example.com
Job Title: Operations Manager
Phone: 555-789-0123

Jennifer (sample) Anderson
Email: jennifer.anderson@example.com
Job Title: Customer Service Rep
Phone: 555-890-1234

Christopher (sample) Thomas
Email: christopher.thomas@example.com
Job Title: Research Analyst
Phone: 555-901-2345

Amanda (sample) Garcia
Email: amanda.garcia@example.com
Job Title: Legal Counsel
Phone: 555-012-3456

Let me know if you need further assistance!
```

Let's update the contacts, since the country is not filled.

```
I forgot to add the country to the contacts in Dataverse. Can you please add the country United States to all 10 contacts?
```

This will update the items in our contacts table.

> [!NOTE]
> Depending on the model used, it can sometimes fail the update because of not having the correct contactid GUIDs. You can easily solve this by sending the prompt 'Please get the IDs from the contacts table'.

![](./assets/updated-items.png)

To verify the actions, run the following prompt:

```
Can you list all contacts in Dataverse with their respective countries?
```

This should lead to a response like this:

![List contacts with country](./assets/list-items-country.png)

## 🗣️ Feedback

In the upcoming months we will add more labs to this repository, so please stay tuned! Hopefully you liked the lab. Please take the time to fill in our [feedback form](https://aka.ms/Dataverse/MCP/Lab/Feedback) to tell us how we can improve!

## ✅ End of the labs!

You finished the labs! Make sure to try out the Dataverse MCP server in your day to day work!

👉 Go back to the [lab readme](../README.md)
