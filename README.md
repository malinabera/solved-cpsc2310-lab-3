Download Link: https://assignmentchef.com/product/solved-cpsc2310-lab-3
<br>
The goal of this lab is to give you practice with pointers, and structs.

<h1>Lab Instructions</h1>

Consider the following snippet of code:




struct NODE{

int a;

struct NODE *b;

struct NODE *c;

};




struct NODE    nodes[5] = {

{20,      nodes + 3,        NULL},

{59,      nodes + 2,        nodes + 4},

{8,        NULL,               nodes + 1},

{44,      nodes + 4,        nodes},

{32,      nodes + 1,        nodes + 3}

};




struct NODE  *np  = nodes + 2;

struct NODE  **npp = &amp;nodes[1].b;







<strong>ALL ANSWERS ON THIS DOCUMENT ARE TO BE IN RED. IF YOU DO NOT USE RED 10 POINTS WILL BE DEDUCTED. </strong>

<strong>Task 1 – 15% of the overall lab grade:</strong>

Fill in the boxes below with the addresses and values for the nodes array. Using the boxes below you are to draw the representation of the nodes array declared above (including variables and their values). This will help you complete the remainder of this lab.

<strong>I have given you the address of the first element of the array. Pretend the integers and pointers are each 4 bytes. Fill in the address for each of the remaining elements of the array. </strong>Obviously, these addresses are not real addresses, but you will use them to determine the values of the expressions below.




With the above you should have all needed information to complete this diagram. Addresses are shown in Hexadecimal. Any answers that is suppose to be an address you must preface with 0x.

Address 200            Address 212              Address 224             Address 236             Address 248

<table>

 <tbody>

  <tr>

   <td width="125">a = 5 (204)  b = nodes + 3= 236 (208)  c = NULL(20  </td>

   <td width="125">a = 15 (212)  b = nodes + 4= 248 (216)  c = nodes + 3= 236 (220) </td>

   <td width="125">a = 22 (224)  b = NULL (228)   c = nodes + 4= 248 (232)  </td>

   <td width="125">a = 12 (236)  b = nodes + 1= 212 (240)  c = nodes= 200 (244)  </td>

   <td width="125">a = 18 (248)  b = nodes + 2= 224 (252)  c = nodes + 1= 212 (256) </td>

  </tr>

 </tbody>

</table>

nodes [0]                  nodes [1]                   nodes [2]                  nodes [3]                 nodes [4]







<strong>Task 2 – 75% of the overall lab grade:</strong>

You will need to evaluate each expression to determine the value. If the expression cannot be evaluated enter ILLEGAL and explain why you think it is illegal. If the expression can be evaluated but with the given information there is no way for you to know the value, enter DO NOT KNOW. Each expression below is independent, you should evaluate each expression with the original values shown (In other words do not use the results of one expression to evaluate the next expression.)













Using the above information, complete the following chart.




<strong><u>Expression                                                      Value</u></strong>







nodes                                       200

nodes.a                                    ILLEGAL

nodes[3].a                               12

nodes[3].c                               200

nodes[3].c-&gt;a                          5

*nodes.a                                  ILLEGAL

(*nodes).a                               5

nodes-&gt;a                                 5

nodes[3].b-&gt;b                          248

&amp;nodes                                    200

&amp;nodes[3].a                            236

&amp;nodes[3].c                             DO NOT KNOW

&amp;nodes[3].c-&gt;a                       200

&amp;nodes-&gt;a                               200

np                                            224

np-&gt;a                                       22

np-&gt;c-&gt;c-&gt;a                             15

npp                                          DO NOT KNOW

npp-&gt;a                                     ILLEGAL

*npp                                        248

*npp-&gt;a                                   ILLEGAL

(*npp)-&gt;a                                18

&amp;np                                         DO NOT KNOW

&amp;np-&gt;a                                    224

&amp;np-&gt;c-&gt;c-&gt;a                          212




<strong>Task 3 – 10% of the overall lab grade:</strong>

Once you have evaluated each expression you are required to write a program, in C, that will print out the value of each legal expression.  Name the “C” file lab3.c.

The format of the output should be the expression, a tab, and the output. The expressions in the blanks above, that produce an address, obviously will not be the same address as the one you print out.




So, you are probably wondering why you don’t just write the program and copy the output to the blanks above. Good question! Some of the expressions above will rely on you knowing what will print in order to even write the print statement.  Also, if you do this you will not learn what you are supposed to learn from this lab. Lastly, you will see some of these or questions like these on exam 1.




In your lab3.c file you must have a comment block that has the following information.




/***********************

*Your name Annie Hayes

*Your username ahayes5

*Lab 3 and your lab section Lab 3 – lab section 003

**********************/