# Shift operators in C++
## *In this tutorial, we are gonna discuss what are Bit-wise shift operators which are used during program execution to shift the Binary digit of a decimal number using the right-shift operator<code>&gt;&gt;</code>and left shift operator<strong><code>&lt;&lt;*</code>


<h2>Bitwise Operators</h2>
<p style="text-align: left;"><span data-preserver-spaces="true">For performing various mathematics operations during program execution in </span><em><span data-preserver-spaces="true">ALU(Arithmetic Logic Unit)</span></em><span data-preserver-spaces="true"> i.e inside the CPU we have to use Bit-wise Operators to perform bit-level operations.</span></p>

### The various type of Bit wise Operators are :

1. &amp;    Bitwise AND
2. |     Bitwise OR
3. ^    Bitwise XOR
4. ~    Bitwise complement
5.  &lt;&lt;  Shift left
6.  &gt;&gt;  Shift right
<h2 style="text-align: left;">Shift Operators</h2>
<span data-preserver-spaces="true">Shift Operators have two types: logical right-shift and arithmetic right-shift. A left-shift is denoted by the </span><strong><span data-preserver-spaces="true">&lt;&lt;</span></strong><span data-preserver-spaces="true"> operator, while a right-shift is denoted by the </span><strong><span data-preserver-spaces="true">&gt;&gt;</span></strong><span data-preserver-spaces="true"> operator.</span>

<span data-preserver-spaces="true">Before we learn Bitwise shift operators we have to know </span><em><span data-preserver-spaces="true">Binary Representations</span></em><span data-preserver-spaces="true"> and </span><em><span data-preserver-spaces="true">Decimal Representations.</span></em>

<span data-preserver-spaces="true">In Decimal Representation, the digits are in the range of 0-9. In Binary Representation, computers use only the digits </span><strong><span data-preserver-spaces="true">0</span></strong><span data-preserver-spaces="true"> and </span><strong><span data-preserver-spaces="true">1. </span></strong><span data-preserver-spaces="true">and the digits are multiples of power of </span><strong><em><span data-preserver-spaces="true">2</span></em></strong><span data-preserver-spaces="true">. The Binary digit has two states </span><strong><span data-preserver-spaces="true">0</span></strong><span data-preserver-spaces="true"> or </span><strong><span data-preserver-spaces="true">1 </span></strong><span data-preserver-spaces="true"> we say it </span><strong><em><span data-preserver-spaces="true">bit</span></em></strong>

<span data-preserver-spaces="true">In binary, we have Unsigned Integer Type</span>
> unsigned char       :    8 bits
Range[0,255]

> unsigned short  :   16 bits
 Range[0, 65,535]

> unsigned int   :  32 bits
 Range[0 , 4,294,967,295]
 
> unsigned long long       :   64 bits
 Range[0 , 18,446,744,073,709,551,615]
 
During the shift operation when we are shifting to the left the leftmost digit in the binary system which we say as the most significant bit is lost and the next binary bit is inserted to the rightmost end. For example, click here <a href="https://photos.app.goo.gl/ohfjyjqm4PGbCnDS7" target="_blank" rel="noopener noreferrer">Diagram</a>
<pre>   0 , 1 , 0 , 1 , 0 
           |
           |
           v</pre>
<strong style="font-family: Georgia, 'times new roman', 'bitstream charter', Times, serif;"> &lt;&lt;
</strong>
<pre>           |
           |
           v
   1 , 0 , 1 , 0 , 0</pre>
   
### Code for Left shift Operation
<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;iostream&gt;
using namespace std;
int main()
 {
   int first = 2;
   first = first &lt;&lt; 3;
   cout &lt;&lt; first &lt;&lt; endl;
   return 0;
 }</pre>
Output :
<pre>16</pre>
In the above the code earlier the value of first was assigned 2 in Binary it represents <span class="com">0000 0010 after left shifting <strong><code>&lt;&lt;</code></strong> the binary value changes to 0001 0000 as it shifts 3 bits left side </span>
<pre>2  - 0000 0010 Before Shifting 
16 - 0001 0000 After Shifting 3 bits</pre>
<h3>Right Shift :  <em><strong><code>&gt;&gt;</code></strong></em></h3>
During the shift operation when we are shifting to the right the rightmost digit in a binary system which we say as the most significant bit is lost and the next binary bit is inserted to the rightmost end. For example, click here <a href="https://photos.app.goo.gl/RscXveXw95TYDeR99" target="_blank" rel="noopener noreferrer">Diagram</a>
<h4>Code for Right shift operation</h4>
<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;iostream&gt;
using namespace std;
int main() 
{
   int second = 8;
   second = second &gt;&gt; 2;
   cout &lt;&lt; second &lt;&lt; endl;
   return 0;
}</pre>
Output :
<pre>2</pre>
<span data-preserver-spaces="true">In the above, the code earlier the value for the variable second was assigned 8 in Binary it represents 0000 1000 after left shifting </span><strong><span data-preserver-spaces="true">&gt;&gt;</span></strong><span data-preserver-spaces="true"> the binary value changes to 0000 0010 as it shifts 2 bits right side.</span>
<h2>C++ Program to perform Shift Operators</h2>
<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;iostream&gt;
void PrintBinaryAndDecimal(unsigned int uiNumber)
   {
       using namespace std;
       cout&lt;&lt;"Bin = ";
       for(int i=31; i&gt;=0;i--)
       {
           std::cout&lt;&lt;(((uiNumber&gt;&gt;i)%2)?'1':'0');
       }
       cout&lt;&lt;" : Decimal = "&lt;&lt;uiNumber&lt;&lt;endl&lt;&lt;endl;
   } 

int main()
{
    using namespace std;
    unsigned int uiNumber = 38;
    cout<<"Original : "<<endl; 
    PrintBinaryAndDecimal(uiNumber); 
    cout<<"Left-Shifted : "<<endl; 
    PrintBinaryAndDecimal(uiNumber<<1);
    cout<<"Right-Shifted :"<<endl; 
    PrintBinaryAndDecimal(uiNumber>>1);    
    cin.get(); 
    return 0; }
}</pre>
Output :
<pre>Original : 
Bin = 00000000000000000000000000100110 : Decimal = 38
Left-Shifted : 
Bin = 00000000000000000000000001001100 : Decimal = 76
Right-Shifted :
Bin = 00000000000000000000000000010011 : Decimal = 19</pre>
&nbsp;

<!--more-->
## For More Content : 
1. <p class="media-heading post-title"><a href="https://www.codespeedy.com/bitwise-operators-in-c-or-cpp/">Bitwise Operators in C or C++</a>

2. <a href="https://www.codespeedy.com/break-and-continue-in-cpp/">Break and Continue Statement in C++</a></p>
