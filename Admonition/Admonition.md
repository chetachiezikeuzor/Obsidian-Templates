```<%* 
newLine = "\n";
const admonitionType = await tp.system.suggester(["📰 Abstract","❗️ Attention","🪲 Bug","🚧 Caution","✅ Check","✏️ Cite","📌 Clipped","🌋 Danger","👍🏽 Done","🙅🏽‍♀️ Error","📄 Example", "❌ Failure", "📃 FAQ", "📍 Help","💡 Hint","🕒 Important","ℹ️ Info","🔍 Missing","📝 Note","❓Question","💬 Quote","🏁 Success","📖 Summary","⚡️ Tip","⏹ Todo","☠️ Warning"],  ["abstract","attention","bug","caution","check","cite","clipped","danger","done", "error", "example", "failure","faq","help","hint","inportant","info","missing","note","question","quote", "success", "summary", "tip", "todo", "warning"]) %>ad-<%* tR += admonitionType %>
<%*
    const title = await tp.system.prompt("Enter Title (Optional)");
	const collapse = await tp.system.suggester(["Collapse", "No Collapse"], ["collapse: true", " "]);
    if(title){
-%>
title:<%* tR += title + newLine + collapse%>
<%*
    }else{
	return;
	}
%>
<% tp.file.selection() %>
```
