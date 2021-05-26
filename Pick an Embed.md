<%* 
item = await tp.system.suggester(["Local Image", "External Image", "Local Video", "External Video"], ["Local Image", "External Image", "Local Video", "External Video"]);

if(item == "Local Image"){
	let itemInput = await tp.system.prompt("Image File Path?"); 
	let itemConf = itemInput;
	itemConf = itemConf.replace(/ /g, '%20');
	return "<img src='file://" + itemConf + "' width='100%' height='auto'>";
}else if(item == "External Image") {
	let itemInput = await tp.system.prompt("Image URL?"); 
	let itemConf = itemInput;
	itemConf = itemConf.replace(/ /g, '%20');
	return "<img src='" + itemConf + "' width='100%' height='auto'>";
}else if(item == "Local Video") {
	let itemInput = await tp.system.prompt("Video File Path?"); 
	let itemConf = itemInput;
	itemConf = itemConf.replace(/ /g, '%20');
	return "<video src='file://" + itemConf + "' width='100%' height='450' controls></video>";
}else if(item == "External Video") {
	videoItem = await tp.system.suggester(["YouTube", "Loom"], ["YouTube", "Loom"]);
		let videoInput = await tp.system.prompt("Video URL?"); 	
		if(videoItem == "YouTube"){
			let itemConf = videoInput;
			itemConf = itemConf.replace(/ /g, '%20');
			newConf = itemConf.replace('watch?v=', 'embed/');
			return "<iframe width='100%' height='450' src='" + newConf + "' frameborder='0' allow='accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture' allowfullscreen style='border: 3px solid #ffbaeb;'></iframe>";
		}else if(videoItem == "Loom"){
			let itemConf = videoInput;
			itemConf = itemConf.replace(/ /g, '%20');
			newConf = itemConf.replace('share/', 'embed/');
			return "<iframe width='100%' height='450' src='" + newConf + "' frameborder='0' allow='accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture' allowfullscreen style='border: 3px solid #ffbaeb;'></iframe>";
		}
} %>
