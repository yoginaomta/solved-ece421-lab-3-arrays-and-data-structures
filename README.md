Download Link: https://assignmentchef.com/product/solved-ece421-lab-3-arrays-and-data-structures
<br>
<strong>Arrays and Data Structures </strong>

Consider the following code:

fn main(){

let mut groups = [[“”; 4]; 6];  groups[0]=[“Bob”, “Carol”, “Eric”, “Matt”];    groups[1]=[“Jim”, “Lucy”, “Terry”, “Brenda”];  groups[2]=[“Susan”, “Brad”, “Jim”, “Matt”];  groups[3]=[“Sue”, “Wendy”, “Sam”, “Brad”];  groups[4]=[“Kate”, “Jack”, “James”, “Sydney”];  groups[5]=[“Mary”, “John”, “Ricky”, “Wendy”];




}

This main function contains the names of the members in six research group.

<strong>Question 1:</strong> You need to write a new function called <em>searchMember</em> to search for a member and report the following information:

<ul>

 <li>Their name’s existence in the list (yes or not)</li>

 <li>Their “group number” (some members are in more than one group)</li>

 <li>Whether they are a group leader (the first person listed in each group is indicated as its leader)</li>

</ul>

<strong>DEMO this deliverable to the lab instructor. </strong>

<h1>Binary Tree</h1>

A binary tree is a tree data structure in which each node has at most two children, which are referred to as the <em>left</em> child and the <em>right</em> child. In other words, each node in a binary tree:

<ul>

 <li>must have a value</li>

 <li>may or may not have left and/or right child One can describe a single node as follows:</li>

</ul>

<table width="628">

 <tbody>

  <tr>

   <td width="628">#[derive(Debug)] struct TreeNode {     data: &amp;str,left_child: Option&lt;TreeNode&gt;,     right_child: Option&lt;TreeNode&gt;, }</td>

  </tr>

 </tbody>

</table>

<strong>Question 2:</strong> Try to run the above code. Does it run? If not, explain why and rewrite the code so it runs.

<ul>

 <li><strong>DEMO this deliverable to the lab instructor. </strong></li>

</ul>

<strong>Question 3:</strong> Write insert_node function that inserts a node with a given value. You can use the following code snippet.

1







ECE 421 | Exploring Software Development Domains




<table width="628">

 <tbody>

  <tr>

   <td width="628">    pub fn insert_node(&amp;self, data: &amp;str) {if self.data == data {             return}let new_node = if data &lt; self.data { &amp;self.left_child } else {&amp;self.right_child };         match …………} </td>

  </tr>

 </tbody>

</table>

<ul>

 <li><strong>DEMO this deliverable to the lab instructor. </strong></li>

</ul>

<strong>Question 4:</strong> Let’s assume your TreeNode struct is replaced with the following Tree enum:

<table width="628">

 <tbody>

  <tr>

   <td width="628">#[derive(Debug)] enum Tree&lt;T: Ord&gt; {Node {               data: T,left_child: Box&lt;Tree&lt;T&gt;&gt;,right_child: Box&lt;Tree&lt;T&gt;&gt;,},Empty,}</td>

  </tr>

 </tbody>

</table>

What changes do you need to make to your insertion code to run the code?

What is the purpose of Empty?

Which solution (struct-based or enum-based) is better?