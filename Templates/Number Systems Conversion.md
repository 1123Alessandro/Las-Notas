# Convert to base 10

<%*
let base = 2;
let length = 5;
let frac = 0;
let x = tp.user.random_number(base, length, frac);
let b10 = tp.user.base10(base, x);
-%>
<% '$$' + x + '_{' + base + '}$$' %>
,,
<% '$$' + b10 + '_{' + 10 + '}$$' %>

<%*
base = 2;
length = 6;
frac = 0;
x = tp.user.random_number(base, length, frac);
b10 = tp.user.base10(base, x);
-%>
<% '$$' + x + '_{' + base + '}$$' %>
,,
<% '$$' + b10 + '_{' + 10 + '}$$' %>

<%*
base = 2;
length = 5;
frac = 0;
x = tp.user.random_number(base, length, frac);
b10 = tp.user.base10(base, x);
-%>
<% '$$' + x + '_{' + base + '}$$' %>
,,
<% '$$' + b10 + '_{' + 10 + '}$$' %>

<%*
base = 16;
length = 5;
frac = 0;
x = tp.user.random_number(base, length, frac);
b10 = tp.user.base10(base, x);
-%>
<% '$$' + x + '_{' + base + '}$$' %>
,,
<% '$$' + b10 + '_{' + 10 + '}$$' %>