```<%* 
newLine = "\n";
const admonitionType = await tp.system.suggester(["π° Abstract","βοΈ Attention","πͺ² Bug","π§ Caution","β Check","βοΈ Cite","π Clipped","π Danger","ππ½ Done","ππ½ββοΈ Error","π Example", "β Failure", "π FAQ", "π Help","π‘ Hint","π Important","βΉοΈ Info","π Missing","π Note","βQuestion","π¬ Quote","π Success","π Summary","β‘οΈ Tip","βΉ Todo","β οΈ Warning"],  ["abstract","attention","bug","caution","check","cite","clipped","danger","done", "error", "example", "failure","faq","help","hint","inportant","info","missing","note","question","quote", "success", "summary", "tip", "todo", "warning"]) %>ad-<%* tR += admonitionType %>
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
