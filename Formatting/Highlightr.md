<%* 
selection = tp.file.selection();
cursor = tp.file.cursor(0);
const highlightr = await tp.system.suggester(["🦋 Blue","🌿 Green","🐰 Grey","🍊 Orange","🌸 Pink","🦄 Purple","🍓 Red","🌼 Yellow"], ["blue","green","grey","orange","pink","purple","red","yellow"]);

return "<mark class='" + highlightr + "' >" + selection + cursor + "</mark>";
%>
