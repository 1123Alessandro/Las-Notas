<%*
let x = await tp.system.prompt('Header number', '1', true, false);
let y = await tp.system.prompt('Text', '', true, false);
let s = '<h' + x + ' style="text-align: center; color: black;">' + y + '</h' + x + '>'
-%>
<% s %>

