
<%* let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(title);
  } 
-%>
<%*
  let title_uppercase = title.replace(/\b\w/g, c => c.toUpperCase());
  let result = title_uppercase.replace(/[^a-zA-Z0-9 ]/g, '');
  tR += "---"
%>
id: <% tp.file.creation_date("YYYYMMDDHHmmss") %>
title:  <%* tR += "\"" + result + "\"" %>
created: <% moment(tp.file.creation_date("YYYY-MM-DDTHH:mm:ss.SSSZ")).toISOString() %>
updated: <% moment(tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss.SSSZ")).toISOString() %>
tags: <% await tp.system.prompt("Enter multiple tags like: [tag1, tag2, tag3]") %>
---

Title:: <%* tR += "\"" + result + "\"" %>
Link:: <% await tp.system.prompt("Enter link to the article") %>
Areas:: <% await tp.system.prompt("Enter backlinks to topics - comma separated") %>
Status:: <% await tp.system.suggester(["read", "unread", "partially read"], ["read", "unread", "partially read"]) %>

---

<% tp.file.cursor() %>