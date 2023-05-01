Download Link: https://assignmentchef.com/product/solved-bbm104-assignment-4-stack-priority-queue
<br>
In this assignment, you are going to simulate a vending machine scenario. According to this scenario, you are given several vending parts such as biscuits, chocolates, drinks and so on. In each part of vending machine, there are vending items. You have also token box for store your tokens. There are also different tokens for each part of vending machine.

<h1>2           Background</h1>

<h2>2.1           Stack</h2>

A stack is an Abstract Data Type (ADT), commonly used in most programming languages. It is named stack as it behaves like a real-world stack, for example – a deck of cards or a pile of plates, etc. A real-world stack allows operations at one end only. For example, we can place or remove a card or plate from the top of the stack only. Likewise, Stack ADT allows all data operations at one end only. At any given time, we can only access the top element of a stack.

This feature makes it LIFO data structure. LIFO stands for Last-in-first-out. Here, the element which is placed (inserted or added) last, is accessed first. In stack terminology, insertion operation is called PUSH operation and removal operation is called POP operation. The following figure (Figure 1) depicts a stack and its operations.

Figure 1: Stack and it’s operation

<h2>2.2           Queue</h2>

Queue is an abstract data structure, somewhat similar to Stacks. Unlike stacks, a queue is open at both its ends. One end is always used to insert data (enqueue) and the other is used to remove data (dequeue). Queue follows First-In-First-Out methodology, i.e., the data item stored first will be accessed first. The following figure (Figure 2) depicts a queue and its operations.

Basic operations are as following:

<ul>

 <li>insert / enqueue:This function defines the operation for adding an element into queue.</li>

 <li>remove / dequeue: This function defines the operation for removing an element from queue.</li>

</ul>

In computer science, a priority queue is an abstract data type similar to a regular queue or stack data structure in which each element additionally has a “priority” associated with it. In a priority queue, an element with high priority is served before an element with low priority.

<h1>3           Problem Definition</h1>

<h2>3.1           Scenario</h2>

You are expected to complete tasks that are given tasks.txt according to input files and produce an output file. The informations about parts, items, tokens and tasks are in the input files. In parts.txt file, you are given several parts of vending machine. These parts are modeled as stacks that are following the last-in-first-out policy. And each part has items given in items.txt. Each item should be in corresponding part of vending machine. You have also token box for store your tokens which are given in tokens.txt. This box is modeled as priority queue. In a priority queue, an item with high priority is served before an element with low priority. In this assignment, the higher value token has more priority. If two tokens have the same value, they should serve according to the order in which they were enqueued. In our scenario, you have two different tasks that are BUY and PUT. These will be given in tasks.txt. There may be more than one of each in tasks.txt.

<h2>3.2           Experiment</h2>

Your system will take the input files as parameters that are parts.txt, items.txt, tokens.txt and tasks.txt. The initial status of the parts of the vending machine can be obtain by reading the input from these files. The status of each part should be written into the output file after the tasks are completed.

<h2>3.3           Inputs</h2>

There will be four input files that your program will take as arguments. These are <em>parts.txt</em>, <em>items.txt</em>, <em>tokens </em>and <em>tasks.txt </em>respectively. You are expected to create a program that reads the inputs about vending machine and after completing tasks given in tasks.txt, produces an output file exhibiting the final status of the each parts of vending machine. Details of the files are given below.

3.3.1         Parts

<ul>

 <li>In each part you are given, items are kept.</li>

 <li>Vending machine parts are modeled as stacks that are following the last-in-first-out policy.</li>

</ul>

3.3.2        Items

<ul>

 <li>The initial status of items are given in items.txt according to their corresponding part.</li>

 <li>Each item can be put to the relevant part in the vending machine or bought from the corresponding part.</li>

 <li>Stack policy is applied when putting or buying items.</li>

</ul>

3.3.3        Tokens

<ul>

 <li>Each token can be used for a relevant items. For example you can only use biscuit tokens to buy biscuits.</li>

 <li>Each token value corresponds to 1 relevant item. For example, you can take only 2 biscuits by using T1 token.</li>

 <li>The list of tokens in the tokens.txt file may be given to you in mixed order.</li>

 <li>Your token box is modeled as priority queues. When asked for a token, you should use the highest value inside the token box.</li>

 <li>The initial state of token box is given tokens.txt</li>

</ul>

3.3.4        Tasks

<ul>

 <li>Your tasks are given in tasks.txt</li>

 <li>You can both buy items from the vending machine and put items into the vending machine.</li>

</ul>

Which action you will do is given in the tasks.txt file.

<ul>

 <li>A tasks.txt has the following format:</li>

</ul>

&lt;BUY&gt;&lt;TAB&gt;&lt;PartOfVendingMachine,NumberOfItems&gt;&lt;TAB&gt;…&lt;TAB&gt;

&lt;PartOfVendingMachine,NumberOfItems&gt;

&lt;PUT&gt;&lt;TAB&gt;&lt;PartOfVendingMachine,ItemId,ItemId,…,ItemId&gt;&lt;TAB&gt;….&lt;TAB&gt;

&lt;PartOfVendingMachine, ItemId,ItemId,…,ItemId &gt;

<ul>

 <li>During a task you need to pay attention to the order of putting items to vending machine and taking items from vending machine.</li>

</ul>

<h2>3.4           Output</h2>

You are expected to produce a output. In this output, status of each part of vending machine should be printed. The format of this file is as follows:

&lt;Name of part&gt;

&lt;Item0&gt;

&lt;Item1&gt; …..

&lt;ItemN&gt;

—————

&lt;Name of part&gt;

&lt;Item0&gt;

&lt;Item1&gt; …..

&lt;ItemN&gt;

—————

&lt;Name of part&gt;

&lt;Item0&gt;

&lt;Item1&gt; …..

&lt;ItemN&gt;

—————…..

…..

—————Token Box:

&lt;Token0&gt;

&lt;Token1&gt; …..

&lt;TokenN&gt;

<h2>3.5           Example Run</h2>

<ul>

 <li>Assume that you are given the files in Section 3.3. Reading the inputs from these files, the initial configuration of the vending machine and your token box as shown in Figure 3.</li>

 <li>As seen in the Figure 3, the items read from the items.txt file are put to the corresponding part in order of reading by using stack principle.</li>

 <li>Tokens read from the tokens.txt file are put to token box according to priority queue. As shown in Figure 3, T1 and T3 have same value. Since T1 is earlier than T3 in the reading order, its priority is high.</li>

</ul>

Figure 3: The initial configuration of the parts and token box

<ul>

 <li>According to task.txt file, you should buy 3 biscuits, 2 chocolates and 1 crisps from the vending machine for the first task. As shown in Figure 3 and Figure 5, putting items to corresponding part and taking items from the part are done according to the stack principle.</li>

 <li>When taking any item from the vending machine, get the corresponding token with the highest priority from the token box. If value of the token you get is greater than or equal to the value given in the task, update the value of the token and insert it back to the queue. If it is small, remove the token from the queue and take the corresponding token from the queue for the remaining value. Repeat this until you provide the value given in the task file. The sum of the corresponding token values of each part will be given higher than the value given in the task file.</li>

</ul>

Figure 4: When reading the first task, the status of the token box step by step

<ul>

 <li>After reading the first task, the status of vending machine as in Figure 5.</li>

</ul>

Figure 5: After reading the first task, status of the parts and token box

<ul>

 <li>For the second task, you should put I13, I14 and I15 into biscuits part of vending machine, put I16 and I17 into the chocolates part of vending machine and lastly put I18 and I19 into the drinks part of vending machine. After reading this task, the status of vending machine as in Figure 6:</li>

</ul>

Figure 6: After reading the first task, status of the parts and token box

<ul>

 <li>After the tasks are completed, the output is shown in Figure 7. Please pay attention to the order of your items when printing the status of each part.</li>

</ul>

Figure 7: Status of each parts and token box after the tasks are completed