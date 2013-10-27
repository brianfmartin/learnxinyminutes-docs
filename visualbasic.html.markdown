---
language: Visual Basic
contributors:
    - ["Brian Martin", "http://brianmartin.biz"]
filename: learnvisualbasic.vb
---

```vb
  <pre class="highlight text"><span class="cp">Module Module1</span>

   <span class="cp"> Sub Main()</span>
    <pre class="highlight cpp">
<span class="cm">' A Quick Overview of Visual Basic Console Applications before we dive</span>
        <span class="cm">' in to the deep end.</span>
        <span class="cm">' Apostrophe starts comments.</span>
        <span class="cm">' To Navigate this tutorial within the Visual Basic Complier, I've put</span>
        <span class="cm"> ' together a navigation system.</span>
        <span class="cm"> ' This navigation system is explained however as we go deeper into this</span>
        <span class="cm"> ' tutorial, you'll understand what it all means.</span>
        <span class="o">Console.Title =</span> <span class="o">(</span><span class="s2">&quot;Learn X in Y Minutes&quot;</span><span class="o">)</span>
        <span class="o">Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;NAVIGATION&quot;</span><span class="o">) 'Display </span>
        <span class="o">Console.WriteLine</span><span class="s2"><span class="o"></span><span class="o">(&quot;&quot;</span><span class="o">)</span>
        <span class="o">Console.ForegroundColor =</span> <span class="s2">ConsoleColor.Green</span>
        <span class="o">Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;1. Hello World Output&quot;</span><span class="o"><span class="o">)</span>
        <span class="o">Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;2. Hello World Input&quot;</span><span class="o"><span class="o">)</span>
       <span class="o"> Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;3. Calculating Whole Numbers&quot;</span><span class="o">)</span>
        <span class="o">Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;4. Calculating Decimal Numbers&quot;</span><span class="o">)</span>
       <span class="o"> Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;5. Working Calculator&quot;</span><span class="o">)</span>
       <span class="o"> Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;6. Using Do While Loops&quot;</span><span class="o">)</span>
        <span class="o">Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;7. Using For While Loops&quot;</span><span class="o">)</span>
       <span class="o"> Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;8. Conditional Statements&quot;</span><span class="o">)</span>
       <span class="o"> Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;9. Select A Drink&quot;</span><span class="o">)</span>
       <span class="o"> Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;50. About&quot;</span><span class="o">)</span>
       <span class="o"> Console.WriteLine</span><span class="s2"><span class="o">(</span>&quot;Please Choose A Number From The Above List&quot;</span><span class="o">)</span>
       <span class="nv">Dim</span> <span class="o">selection </span><span class="nv">As String</span><span class="o"> = </span><span class="s2">Console.ReadLine</span>
        <span class="nv">Select Case selection</span>
           <span class="nv"> Case</span><span class="s2"> &quot;1&quot; 'HelloWorld Output</span>
                <span class="o">Console.Clear()</span><span class="cm"> 'Clears the application and opens the private sub</span>
                <span class="o">HelloWorldOutput()</span> <span class="cm">'Name Private Sub, Opens Private Sub</span>
            <span class="nv">Case </span><span class="s2">&quot;2&quot; 'Hello Input</span>
               <span class="o"> Console.Clear()</span>
                <span class="o">HelloWorldInput()</span>
            <span class="nv">Case</span><span class="s2"> &quot;3&quot; 'Calculating Whole Numbers </span>
               <span class="o"> Console.Clear()</span>
               <span class="o"> CalculatingWholeNumbers()</span>
            <span class="nv">Case</span> <span class="s2">&quot;4&quot; 'Calculting Decimal Numbers </span>
                <span class="o">Console.Clear()</span>
               <span class="o"> CalculatingDecimalNumbers()</span>
            <span class="nv">Case</span> <span class="s2">&quot;5&quot; 'Working Calcculator </span>
                <span class="o">Console.Clear()</span>
               <span class="o"> WorkingCalculator()</span>
           <span class="nv"> Case</span> <span class="s2">&quot;6&quot; 'Using Do While Loops</span>
               <span class="o"> Console.Clear()</span>
               <span class="o"> UsingDoWhileLoops()</span>
           <span class="nv"> Case</span> <span class="s2">&quot;7&quot; 'Using For While Loops</span>
                <span class="o">Console.Clear()</span>
                <span class="o">UsingForLoops()</span>
        <span class="nv">    Case</span><span class="s2"> &quot;8&quot; 'Conditional Statements</span>
               <span class="o"> Console.Clear()</span>
                <span class="o">ConditionalStatement()</span>
         <span class="nv">   Case</span><span class="s2"> &quot;9&quot; 'If/Else Statement</span>
               <span class="o"> Console.Clear()</span>
               <span class="o"> IfElseStatement()</span> <span class="cm">'Select a drink</span>
         <span class="nv">   Case</span><span class="s2"> &quot;50&quot; 'About msg box</span>
                <span class="o">  Console.Clear()</span>
                <span class="o">  Console.Title = </span><span class="s2"> (&quot;Learn X in Y Minutes :: About&quot;)</span>
              <span class="s2">   MsgBox(&quot;This tutorial is by Brian Martin (@brianmartinuk&quot;)</span>
                 <span class="o"> Console.Clear()</span>
               <span class="cp"> Main()</span>
               <span class="o">  Console.ReadLine()></span></span>

       <span class="cp">  End Select</span>
   <span class="cp">  End Sub</span>

   <span class="cm"> 'One - I'm using numbers to help with the above navigation when I come back</span>
  <span class="cm">  'later to build it.</span>

   <span class="cm"> 'We use private subs to seperate different sections of the program. </span>
     <span class="cp"> Private Sub HelloWorldOutput()</span>
       <span class="cm"> 'Title of Console Application</span>
       <span class="o"> Console.Title =</span><span class="s2"> &quot;Hello World Ouput | Learn X in Y Minutes&quot;</span>
        <span class="cm">'Use Console.Write(&quot;&quot;) or Console.WriteLine(&quot;&quot;) to print outputs.</span>
        <span class="cm">'Followed by Console.Read() alternatively Console.Readline()</span>
        <span class="cm">'Console.ReadLine() prints the output to the console.</span>
        <span class="o">Console.WriteLine</span><span class="s2">(&quot;Hello World&quot;)</span>
        <span class="o">Console.ReadLine()</span>
    <span class="cp">  End Sub</span>

    <span class="cm">'Two</span>
      <span class="cp"> Private Sub HelloWorldInput()</span>
         <span class="o"> Console.Title =</span><span class="s2"> &quot;Hello World YourName | Learn X in Y Minutes&quot;</span>
        <span class="cm">' Variables</span>
        <span class="cm">' Data entered by a user needs to be stored.</span>
       <span class="cm"> ' Variables also start with a Dim and end with an As VariableType.</span>
        <span class="cm">' In this tutorial, we want to know what your name, and make the program</span>
       <span class="cm"> ' respond to what is said.</span>
       <span class="nv">Dim</span><span class="o"> username </span><span class="nv">As String</span>
       <span class="cm"> 'We use string as string is a text based variable.</span>
        <span class="o">Console.WriteLine</span><span class="s2">(&quot;Hello, What is your name? &quot;)</span><span class="cm"> 'Ask the user their name.</span>
        <span class="s2">username</span> = Console.ReadLine() 'Stores the users name.
        <span class="o">Console.WriteLine</span><span class="s2">(&quot;Hello &quot; + username)</span><span class="cm"> 'Output is Hello 'Their name'</span>
       <span class="o"> Console.ReadLine()</span><span class="s2"> 'Outsputs the above.</span>
        <span class="cm">'The above will ask you a question followed by printing your answer.</span>
        <span class="cm">'Other variables include Integer and we use Integer for whole numbers.</span>
   <span class="cp"> End Sub</span>

    <span class="cm">'Three</span>
   <span class="cp"> Private Sub CalculatingWholeNumbers()</span>
        <span class="o"> Console.Title =</span> &quot;Calculating Whole Numbers | Learn X in Y Minutes&quot;
       <span class="o">  Console.Write</span><span class="s2">(&quot;First number: &quot;)</span><span class="cm">  'Enter a whole number, 1, 2, 50, 104 ect</span>
       <span class="nv">  Dim</span> <span class="s2">a</span><span class="o">  As</span><span class="nv">  Integer</span><span class="o"> = Console.ReadLine()</span>
       <span class="o"> Console.Write</span><span class="s2">(&quot;Second number: &quot;) </span><span class="cm">'Enter second whole number.</span>
        <span class="nv">Dim</span><span class="s2"> b</span><span class="o"> As</span><span class="nv"> Integer</span><span class="o">  = Console.ReadLine()</span>
        <span class="nv">Dim</span><span class="s2"> c</span><span class="o"> As </span><span class="nv">Integer</span><span class="o"> =</span><span class="s2"> a </span><span class="o">+</span><span class="s2"> b</span>
        <span class="o">Console.WriteLine(</span><span class="s2">c</span><span class="o">)</span>
       <span class="o"> Console.ReadLine()</span>
       <span class="cm"> 'The above is a simple calculator</span>
  <span class="cp"> End Sub</span>

   <span class="cm"> 'Four</span>
    <span class="cp"> Private Sub CalculatingDecimalNumbers()</span>
        <span class="o">Console.Title =</span><span class="s2">  &quot;Calculating with Double | Learn X in Y Minutes&quot;</span>
        <span class="cm">'Of course we would like to be able to add up decimals.</span>
       <span class="cm"> 'Therefore we could change the above from Integer to Double.</span>

       <span class="cm"> 'Enter a whole number, 1.2, 2.4, 50.1, 104.9 ect</span>
        <span class="o">Console.Write</span><span class="s2">(&quot;First number: &quot;)</span>
        <span class="nv">Dim</span> <span class="s2"> a</span><span class="o"> As</span><span class="nv"> Double</span> = <span class="o">Console.ReadLine</span>
        <span class="o">Console.Write</span><span class="s2">(&quot;Second number: &quot;)</span><span class="cm">'Enter second whole number.</span>
       <span class="nv">Dim</span> <span class="s2">b</span> <span class="o">As</span><span class="nv"> Double</span> = <span class="o">Console.ReadLine</span>
         <span class="nv">Dim</span> <span class="s2">c</span><span class="o"> As</span><span class="nv"> Double</span><span class="o"> =</span><span class="nv"> a </span><span class="o">+</span> <span class="nv">b</span>
        <span class="o"> Console.WriteLine(</span><span class="s2">c</span><span class="o">)</span>
        <span class="o">Console.ReadLine()</span>
       <span class="cm"> 'Therefore the above program can add up 1.1 - 2.2</span>
     <span class="cp"> End Sub</span>

    <span class="cm">'Five</span>
    <span class="cp"> Private Sub WorkingCalculator()</span>
        <span class="o">Console.Title =</span><span class="s2"> &quot;The Working Calculator| Learn X in Y Minutes&quot;</span>
       <span class="cm"> 'However if you'd like the calculator to subtract, divide, multiple and</span>
        <span class="cm"> 'add up.</span>
         <span class="cm">'Copy and paste the above again.</span>
        <span class="o"> Console.Write(&quot;First number: &quot;)</span>
        <span class="nv"> Dim</span><span class="s2"> a</span> <span class="o">As</span> <span class="nv"> Double</span> <span class="o">= Console.ReadLine</span>
        <span class="o">Console.Write</span><span class="s2">(&quot;Second number: &quot;)</span><span class="cm"> 'Enter second whole number.</span>
        <span class="nv">Dim</span><span class="s2"> b</span> <span class="o"> As</span> <span class="nv">Integer</span><span class="o">  = <span class="s2">Console.ReadLine</span>
        <span class="nv">Dim</span><span class="s2"> c</span> <span class="o"> As</span> <span class="nv">Integer</span><span class="o">  = <span class="s2">a + b</span>
        <span class="nv">Dim</span><span class="s2"> d </span><span class="o"> As</span> <span class="nv">Integer</span><span class="o">  = <span class="s2">a * b</span>
        <span class="nv">Dim</span><span class="s2"> e </span><span class="o">  As</span> <span class="nv">Integer</span><span class="o">  =<span class="s2"> a - b</span>
        <span class="nv">Dim</span><span class="s2"> f</span> <span class="o"> As</span> <span class="nv">Integer</span> <span class="o"> = <span class="s2"> a / b</span>

      <span class="cm">  'By adding the below lines we are able to calculate the subtract,</span>
       <span class="cm"> 'multply as well as divide the a and b values</span>
        <span class="o"> Console.Write(</span><span class="nv">a.ToString() + &quot; + &quot; + b.ToString()</span>)
       <span class="cm"> 'We want to pad the answers to the left by 3 spaces.</span>
       <span class="o">  Console.WriteLine(</span><span class="nv">&quot; = &quot; + c.ToString.PadLeft(3)</span>)
        <span class="o"> Console.Write(</span><span class="nv">a.ToString() + &quot; * &quot; + b.ToString()</span><span class="o">)</span>
        <span class="o"> Console.WriteLine(</span><span class="nv">&quot; = &quot; + d.ToString.PadLeft(3)</span><span class="o">)</span>
        <span class="o"> Console.Write(</span><span class="nv">a.ToString() + &quot; - &quot; + b.ToString()</span><span class="o">)</span>
       <span class="o">  Console.WriteLine(</span><span class="nv">&quot; = &quot; + e.ToString.PadLeft(3)</span><span class="o">)</span>
        <span class="o"> Console.Write(</span><span class="nv">a.ToString() + &quot; / &quot; + b.ToString()</span><span class="o">)</span>
        <span class="o"> Console.WriteLine(</span><span class="nv">&quot; = &quot; + e.ToString.PadLeft(3)</span><span class="o">)</span>
        <span class="o"> Console.ReadLine()</span>

    <span class="cp">End Sub</span>

  <span class="cm">  'Six</span>
   <span class="cp"> Private Sub UsingDoWhileLoops()</span>
       <span class="cm"> 'Just as the previous private sub</span>
       <span class="cm">  'This Time We Ask If The User Wishes To Continue (Yes or No?)</span>
       <span class="cm">  'We're using Do While Loop as we're unsure if the user wants to use the</span>
        <span class="cm"> 'program more than once.</span>
        Console.Title = <span class="s2">&quot;UsingDoWhileLoops | Learn X in Y Minutes&quot;</span>
        <span class="nv">Dim</span> answer As String 'We use the variable &quot;String&quot; as the answer is text
       <span class="nv"> Do </span><span class="cm">'We start the program with </span>
            Console.Write(&quot;First number: &quot;)
            <span class="nv">Dim</span> a As Double = Console.ReadLine
            Console.Write(&quot;Second number: &quot;)
            <span class="nv">Dim</span> <span class="s2">b </span>As <span class="nv">Integer</span> = Console.ReadLine
            <span class="nv">Dim</span> <span class="s2">c </span>As <span class="nv">Integer</span> =<span class="s2"> a + b</span>
            <span class="nv">Dim</span> <span class="s2">d</span> As <span class="nv">Integer</span> =<span class="s2"> a * b</span>
            <span class="nv">Dim</span> <span class="s2">e </span>As <span class="nv">Integer</span> =<span class="s2"> a - b</span>
            <span class="nv">Dim</span> <span class="s2">f </span>As <span class="nv">Integer</span> =<span class="s2"> a / b</span>

            Console.Write(<span class="nv">a.ToString() + &quot; + &quot; + b.ToString()</span>)
            Console.WriteLine(<span class="nv">&quot; = &quot; + c.ToString.PadLeft(3)</span>)
            Console.Write(<span class="nv">a.ToString() + &quot; * &quot; + b.ToString()</span>)
            Console.WriteLine(<span class="nv">&quot; = &quot; + d.ToString.PadLeft(3)</span>)
            Console.Write(<span class="nv">a.ToString() + &quot; - &quot; + b.ToString()</span>)
            Console.WriteLine(<span class="nv">&quot; = &quot; + e.ToString.PadLeft(3)</span>)
            Console.Write(<span class="nv">a.ToString() + &quot; / &quot; + b.ToString()</span>)
            Console.WriteLine(<span class="nv">&quot; = &quot; + e.ToString.PadLeft(3)</span>)
            Console.ReadLine()
            <span class="cm">'Ask the question, does the user wish to continue? </span>
            <span class="cm">'Unfortunately it is case sensitive. </span>
            Console.Write(&quot;Would you like to continue? (yes / no)&quot;)
            <span class="cm">'The program grabs the variable and prints and starts again.</span>
            <span class="nv">answer</span> = Console.ReadLine
        <span class="cm">'The command for the variable to work would be in this case &quot;yes&quot;</span>
        Loop <span class="nv">While</span> answer = &quot;yes&quot;

    
 <span class="cp"> End Sub</span>

    <span class="cm">'Seven</span>
     <span class="cp">Private Sub UsingForLoops()</span>
      <span class="cm">  'Sometimes the program only needs to run once.</span>
       <span class="cm"> 'In this program we'll be counting down from 10.</span>

        Console.Title = <span class="s2">&quot;Using For Loops | Learn X in Y Minutes&quot;</span>
      <span class="cm">  'Declare Variable and what number it should count down in Step -1, </span>
        <span class="cm">'Step -2, Step -3 ect. </span>
        For <span class="nv">i</span> As Integer = 10 To 0 Step -1 
            Console.WriteLine(i.ToString) <span class="cm">'Print the value of the counter</span>
        Next <span class="nv">i </span><span class="cm">'Calculate new value</span>
        Console.WriteLine(&quot;Start&quot;) <span class="cm">'Lets start the program baby!!</span>
        Console.ReadLine() <span class="cm">'POW!! - Perhaps I got a little excited then :)</span>

 <span class="cp"> End Sub</span>

   <span class="cm"> 'Eight</span>
   <span class="cp">  Private Sub ConditionalStatement()</span>
        Console.Title = <span class="s2">&quot;Conditional Statements | Learn X in Y Minutes&quot;</span>
         <span class="nv">Dim userName</span> As  <span class="nv">String</span> = Console.ReadLine
        Console.WriteLine(&quot;Hello, What is your name? &quot;) <span class="cm">'Ask the user their name.</span>
         <span class="nv">userName</span> = Console.ReadLine()<span class="cm"> 'Stores the users name.</span>
       <span class="nv"> If</span> userName = &quot;Adam&quot; Then
            Console.WriteLine(<span class="s2"> &quot;Hello Adam&quot;</span>)
            Console.WriteLine(<span class="s2"> &quot;Thanks for creating this useful site&quot;</span>)
            Console.ReadLine()
        <span class="nv">Else</span>
            Console.WriteLine(<span class="s2"> &quot;Hello &quot; + userName</span>)
            Console.WriteLine(<span class="s2"> &quot;Have you checked out www.learnxinyminutes.com&quot;</span>)
            Console.ReadLine() <span class="cm">'Ends and prints the above statement.</span>
        <span class="nv">End If</span>

 <span class="cp"> End Sub</span>

  <span class="cm">  'Nine</span>
    <span class="cp"> Private Sub IfElseStatement()</span>
    Console.Title =<span class="s2"> &quot;If / Else Statement | Learn X in Y Minutes&quot;</span>
        <span class="cm">'Sometimes its important to consider more than two alternatives.</span>
       <span class="cm"> 'Sometimes there are a good few others.</span>
        <span class="cm">'When this is the case, more than one if statement would be required.</span>
        <span class="cm">'An if statement is great for vending machines. Where the user enters a code.</span>
        <span class="cm">'A1, A2, A3, ect to select an item.</span>
        <span class="cm">'All choices can be combined into a single if statement.</span>

        <span class="nv">Dim </span>selection As<span class="nv"> String</span> = Console.ReadLine 'Value for selection
            Console.WriteLine(<span class="s2">&quot;A1. for 7Up&quot;</span>)
            Console.WriteLine(<span class="s2">&quot;A2. for Fanta&quot;</span>)
            Console.WriteLine(<span class="s2">&quot;A3. for Dr. Pepper&quot;</span>)
            Console.WriteLine(<span class="s2">&quot;A4. for Diet Coke&quot;</span>)
            Console.ReadLine()
            <span class="nv">If</span> selection = &quot;A1&quot; <span class="nv">Then</span>
                Console.WriteLine(<span class="s2">&quot;7up&quot;</span>)
                Console.ReadLine()
            <span class="nv">ElseIf</span> selection = &quot;A2&quot; <span class="nv">Then</span>
                Console.WriteLine(<span class="s2">&quot;fanta&quot;</span>)
                Console.ReadLine()
            <span class="nv">ElseIf</span> selection = &quot;A3&quot; <span class="nv">Then</span>
                Console.WriteLine(<span class="s2">&quot;dr. pepper&quot;</span>)
                Console.ReadLine()
            <span class="nv">ElseIf</span> selection = &quot;A4&quot; <span class="nv">Then</span>
                Console.WriteLine(<span class="s2">&quot;diet coke&quot;</span>)
                Console.ReadLine()
            <span class="nv">Else</span>
                Console.WriteLine(<span class="s2">&quot;Please select a product&quot;</span>)
                Console.ReadLine()
            <span class="nv">End If</span>


 <span class="cp"> End Sub</span>

<span class="cp">End Module</span>

</pre>
```

## References

I learnt Visual Basic in the console application. It allowed me to understand the principles of computer programming to go on to learn other programming languages easily. 

I created a more indepth <a href="http://www.vbbootcamp.co.uk/" Title="Visual Basic Tutorial">Visual Basic tutorial</a> for those who would like to learn more. 

The entire syntax is valid. Copy the and paste in to the Visual Basic compiler and run (F5) the program. 
