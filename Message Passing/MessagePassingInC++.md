# Message Passing in C++

## *Message Passing the Topic itself gives a meaning <em>"Passing something". </em>So in this topic we are gonna learn What is Message Passing ? and How it Works in C++.*

### From the basics of Object-Oriented Programming Concepts, we will see how an object is Pass through its class and call by the user with some good examples related to our real-life problems.
<h2>What is a Message?</h2>

<b><i>A request for an object to perform one of its operations is called a message.</b></i> Operation means method/function. A message cannot go automatically it creates an interface, which means it creates an interface for an object. The interface provides the abstraction over the message means hide the implementation. So we get to know,
<em>An interface is a set of operations that a given object can perform

<strong>All communication between objects is done via message is called message passing</strong>, as people exchange information similarly the sending and receiving of information by the object is said to be message passing, to make possible message passing the following things have to be followed to be done :
<blockquote>
<ul>
 	<li>We have to create classes that define objects and its behaviour.</li>
 	<li>Then Creating the objects from class definitions</li>
 	<li>Calling and connecting the communication among objects</li>
</ul>
</blockquote>
<h2>Real word Examples :</h2>

### <b><i>Sending Message to Object -</b></i>

Example: we want to move a car fast we will accelerate it :
<blockquote>
<pre>move a car faster (press accelerator())
Press accelerator ----&gt; send some message to car object ----&gt; call its function(accelerate) ----&gt; perfrom its task of moving
stop ---&gt;&gt; Brakes (stopping the car)   ----&gt;stopTheCar()</pre>
</blockquote>
Another in our real life we want to withdraw money from ATM so
<blockquote>
<pre>withdraw money ATM(press or touch or click the withdraw option ---&gt; send some message to object ATM ----&gt; call its method or function withDrawMoney() ---&gt; task()</pre>
</blockquote>
There could be another function which you can use in ATM-like we can
<blockquote>
<pre>changePIN(), changeMobile() , generateStatement() , transfer() etc.</pre>
</blockquote>
So in every case, we are sending messages or passing some message of sending some message and all these are implemented using member function call.
<blockquote>
<pre>Message  --------&gt;   member function calls</pre>
</blockquote>
So we can say that there are some behavior or capabilities that are achieved by an object and we implement using member function.
<blockquote>
<pre>Behaviours (capabilities)   -----&gt;   member functions (methods)</pre>
</blockquote>
we have some attributes or some properties of object and we are going to specify these using data members or variables.
<blockquote>
<pre>Attributes (Properties)     -----&gt;   data members(variables)</pre>
</blockquote>
<h3>Basic Code for Message Passing :</h3>
<blockquote>&nbsp;
<pre class="EnlighterJSRAW" data-enlighter-language="cpp" data-enlighter-linenumbers="false">class A
{
    public void Methodname(Object obj)
    {
        // Method does something which you assigned to do
    }
}

class B
{
    Object obj1 = new Object();

    A a = new A();
    a.Method1(obj1);
}</pre>
&nbsp;

In the code passing parameter (obj1) to Method1 is said to be Message Passing.</blockquote>
