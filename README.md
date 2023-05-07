Download Link: https://assignmentchef.com/product/solved-ipc144-workshop-2-computations
<br>
In this workshop, you will code and execute a C-language program that accepts numerical values from the user, stores the values in variables of appropriate data type, performs calculations on the stored variables and casts from one data type to another.

<h1>LEARNING OUTCOMES</h1>

Upon successful completion of this workshop, you will have demonstrated the abilities:

<ul>

 <li>to declare variables of integral and floating point types</li>

 <li>to code a simple calculation using C operators and expressions</li>

 <li>to accept a numerical value from the user using scanf</li>

 <li>to cast a value from one data type to another</li>

 <li>to describe to your instructor what you have learned in completing this workshop</li>

</ul>




<h1>IN_LAB: DONE IN CLASS</h1>

Download or clone workshop 2 (<strong>WS02</strong>) from <strong><u>https://github.com/Seneca-144100/IPCWorkshops</u></strong>

In the in_lab directory of workshop 2, right-click on the file in_lab.vsxproj and select the “Open With” context menu item then select “Microsoft Visual Studio 2019” to open the workshop in Visual Studio.

In the Visual Studio solution explorer panel, open and write your code in <strong>cashRegister.c</strong> for workshop 2.

Start the program by asking the user to enter the amount due. Print the following message:

<strong>Please enter the amount to be paid: $</strong>

Assume the user enters 8.68, this is what the screen should look like:

(&lt;ENTER&gt; means hitting the enter key)

<table width="395">

 <tbody>

  <tr>

   <td width="298"><strong>Please enter the amount to be paid: $</strong></td>

   <td width="97"><strong>8.68 &lt;ENTER&gt;</strong></td>

  </tr>

 </tbody>

</table>

Read the amount due and store it as a double.

Calculate the number of loonies and quarters required to pay the amount due and display the following:

<strong>Loonies required: 8, balance owing $0.68 Quarters required: 2, balance owing $0.18</strong> Execution and Output Example:

Please enter the amount to be paid: $8.68

Loonies required: 8, balance owing $0.68

Quarters required: 2, balance owing $0.18

For submission instructions, see the <a href="https://scs.senecac.on.ca/~oop244/pages/workshops/w2.html#sub">SUBMISSION</a> section below.

<strong>IN_LAB SUBMISSION:</strong>

To test and demonstrate execution of your program use the same data as the output example above.

If not on matrix already, upload your <strong>cashRegister.c</strong> to your matrix account. Compile and run your code and make sure everything works properly.




<strong>AtThePrompt&gt; gcc -Wall cashRegister.c –o ws&lt;ENTER&gt; </strong>




-Wall activates the display of warnings in GCC compiler.

-o sets the executable name (ws)

Then run the following script from your account: (replace profname.proflastname with your professors Seneca userid and replace <strong>NAA</strong> with your section)

<strong> </strong>

<strong>~profname.proflastname/submit 144w2/NAA_lab &lt;ENTER&gt;  </strong>

<strong> </strong>

and follow the instructions.




<h1>AT_HOME:</h1>

After completing the in_lab section, edit and upgrade <strong>cashRegister.c</strong> to add the GST to the total entered by the user.

Display the amount of the GST and then the total due. Then display the number of quarters, dimes, nickels and pennies required to pay the total amount.

Problem: 8.68 * .13 is equal to 1.1284, which should be rounded up to 1.13, and the format specifier %.2lf will display as 1.13, but the number will be truncated to 1.12 on a C standard compiler, such as matrix, if we multiply by 100 and cast to an int, which we must do at some point in the program.

To find the correct value for GST do the following:

GST = amountOwing * .13 + .005; (result is 1.1334 which will resolve to 1.13 when either rounded or truncated)

After Calculating the number of loonies required, subtract the number of loonies from the amountOwing, then cast the remaining decimal portion to an int. The subsequent operations must be done using <strong>integer division</strong> and <strong>modulus</strong>. Although the answer can be derived without using the modulus operator, failure to use modulus will result in a grade of 0 for the At_Home portion of the workshop.

<em>Hints: </em>

<ul>

 <li><em>Read about casting, division and modulus in the notes </em></li>

 <li><em>35 * 100 = 35 </em></li>

 <li><em>You can output the value 5, stored in an int variable as $0.05 like this: </em>printf(“$%1.2f”, (float)intBalance/100);</li>

</ul>

Execution and Output Example:

<strong>Please enter the amount to be paid: $</strong><strong>8.68</strong><strong> GST: 1.13 Balance owing: $9.81 Loonies required: 9, balance owing $0.81 Quarters required: 3, balance owing $0.06 Dimes required: 0, balance owing $0.06 Nickels required: 1, balance owing $0.01 Pennies required: 1, balance owing $0.00 </strong>

<h1>AT-HOME REFLECTION</h1>

Please provide answers to the following in a text file named <strong>reflect.txt. </strong>

In three or more paragraphs, explain what you learned while doing this workshop. Tell us what was interesting and what you found difficult. Explain why it is often a best practice to convert floating-point values to integers when performing arithmetic operations. Why is it a best practice to use the modulus operator rather than division and subtraction to find a remainder?

<strong>Reflections will be graded on clarity of thought, correctness, grammar and spelling. </strong>

<strong><u>Note</u></strong><strong>: when completing the workshop reflection it is a violation of academic policy to cut and paste content from the course notes or any other published source, or to copy the work of another student.</strong>

<strong> </strong>

<strong>AT_HOME SUBMISSION:</strong>

To test and demonstrate execution of your program using the same data as the output example above.

If not on matrix already, upload your <strong>cashRegister.c</strong> and <strong>reflect.txt</strong> to your matrix account. Compile and run your code and make sure everything works properly.




<strong>AtThePrompt&gt; gcc -Wall cashRegister.c –o ws &lt;ENTER&gt;</strong>

Then run the following script from your account: (replace profname.proflastname with your professors Seneca userid and replace <strong>NAA</strong> with your section)

<h2>~profname.proflastname/submit 144w2/NAA_home &lt;ENTER&gt;</h2>

and follow the instructions.