---


---

<h1 id="variables-in-shell">Variables in Shell</h1>
<p><strong>Variables</strong> in shell are an essential part of managing dynamic values within your. <strong>They act as pointers to data, enabling you to manipulate and utilize values efficiently.</strong></p>
<p>A <strong>shell variable is a named container used to store data in memory while a shell script is running</strong>. Think of it as a labelled box that holds data during script execution. The stored value can be a string, number, filename or even the output of a command. Variables make shell scripts dynamic and flexible instead of hard-coded and static.</p>
<ul>
<li>A <strong>variable</strong> is a character string that represents a value.</li>
<li>It is a <strong>pointer to the actual data stored in memory</strong>.</li>
<li>Shell allows you to create, assign, and delete variables dynamically.</li>
<li>Store temporary data during script execution.</li>
<li>Accept and process user input.</li>
<li>Store the output of commands.</li>
<li>Control decision-making in loops and conditionals.</li>
<li>Pass arguments between scripts and processes.</li>
</ul>
<p><strong>Saves typing and easy to change:</strong><br>
Imagine you write a script that uses the folder path <code>/home/user/projects/my_website</code> 10 times. If you rename that folder later, you would have to fix it in 10 places.</p>
<p><strong>Works with changing information:</strong><br>
Some information changes every time you run a script, like today’s date or the person typing at the keyboard. Variables catch this live data for you.</p>
<h2 id="two-types-of-variable-in-shell-scripting--">Two types of variable in shell scripting :-</h2>
<h2 id="user-defined-variables--">1) User-defined variables :-</h2>
<p>It is created and managed by user’s with user’s script to stop custom date.</p>
<h4 id="valid-variable-names-can-include">Valid Variable names can include:</h4>
<pre><code>-   Letters (`a-z`, `A-Z`),
-   Numbers (`0-9`), and
-   Underscores (`_`).
</code></pre>
<p>ex :-</p>
<pre><code># User define variables
#!/bin/bash

echo "user define variables"
name="Vyas"
age="24"
Name="More"
echo ${name}
echo "${name} ${age}  ${Name}  ${name}"

echo "my name is ${name} and my age is ${age}"
</code></pre>
<p>output :-</p>
<pre><code>user define variables
Vyas
Vyas 24  More  Vyas
my name is Vyas and my age is 24
</code></pre>
<h2 id="system-defined-variables--">2) System-defined variables :-</h2>
<p>system defined variables in shell script are predefined by the linux <strong>BASH Shell</strong> and play a vital role in managing environment configuration, scripts execution and debugging process.</p>
<p>System variables are created and maintained by the Linux shell itself. These variables configure aspects of the shell’s behavior and environment, such as:</p>
<ul>
<li>User details</li>
<li>File paths</li>
<li>System locales</li>
<li>Shell configurations</li>
</ul>
<p>The system variables defined in <strong>UPPERCASE</strong> letter &amp; can be used to extract valuable information about shell environment.</p>
<p>ex :-</p>
<pre><code># System-defined variables

#!/bin/bash
echo "this is system variable"
echo $LINES
echo "User: $USER"
echo "Home Directory: $HOME"
echo "Shell: $SHELL"
echo "Machine Name: $HOSTNAME"
echo "Working Directory: $PWD"
echo "User ID: $UID"
echo "System Path: $PATH"
echo "Operating System: $OSTYPE"
echo "Parent Process ID: $PPID"
echo "Script Runtime: $SECONDS seconds"
echo "Random Number: $RANDOM"
echo "Terminal Dimensions: $LINES lines x $COLUMNS columns"
echo "Temporary Directory: $TMPDIR"
sleep 5
echo "Execute time: $SECONDS"
</code></pre>
<p>output :-</p>
<pre><code>this is system variable
24
User: vyas
Home Directory: /home/vyas
Shell: /bin/bash
Machine Name: rocky-II
Working Directory: /home/vyas/shell-script
User ID: 1000
System Path: /home/vyas/.local/bin:/home/vyas/bin:/usr/lib/jvm/java-21-openjdk/bin:/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin
Operating System: linux-gnu
Parent Process ID: 4506
Script Runtime: 0 seconds
Random Number: 29887
Terminal Dimensions: 24 lines x 80 columns
Temporary Directory:
Execute time: 5
</code></pre>
<h3 id="reading-input-from-user--">Reading Input from User :-</h3>
<p>In **BASH  scripting ** the <code>read</code> commands is a versatile tool that allows you to capture input from users.</p>
<p>Ex, :-</p>
<pre><code># Reading input from user 
#!/bin/bash
read -p "enter your name: " name
read -p "enter your age: " age
echo ${name}
echo "hello ${name} , and your age is ${age}."
</code></pre>
<p>output : -</p>
<pre><code>enter your name: Vyas
enter your age: 24
Vyas
hello Vyas , and your age is 24.
</code></pre>
<h4 id="example-of-username-and-password--">example of username and password :-</h4>
<p><strong>-p</strong> display a prompt message<br>
<strong>-s</strong> secret input  (<strong>silent mode</strong>)</p>
<pre><code>#!/bin/bash  
read -p "Enter your username: " username 
read -p "Enter your password: " password
read -p "Enter your password: " -s password
echo  "Welcome, ${username}!"
</code></pre>
<p>output :-</p>
<pre><code>Enter your username: vyas
Enter your password:password
Enter your password:
Welcome, vyas!
</code></pre>

