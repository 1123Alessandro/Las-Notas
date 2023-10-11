<%*
let s = "```\n"
let j = await tp.system.prompt("Number of Data Samples", '', true, false)
for (let i = 0; i < j; i++) {
	let x = Math.random()*11;
	x = Math.floor(x);
	s += x + ", "
}
s += "\n```"
tR += s
%>