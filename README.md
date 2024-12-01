<h1>BigInt: A New Data Type for Large Integers</h1>

<p>In C/C++, the maximum number of digits a <code>long long int</code> can have is 20. This limitation makes it difficult to store and perform arithmetic operations on numbers that exceed 20 digits. For example, a 22-digit number cannot be stored in any primitive data type. To handle such large numbers, we introduce a new data type called <strong>BigInt</strong>.</p>

<p>The <code>BigInt</code> data type is designed to handle large integers, perform arithmetic operations, and solve problems that require working with big numbers efficiently. This article outlines the basic operations that have been implemented on the new <strong>BigInt</strong> type.</p>

  <h2>Supported Operations</h2>
    <p>The following operations are supported on the <strong>BigInt</strong> data type:</p>
    <ul>
        <li><strong>Addition</strong> of two big integers</li>
        <li><strong>Subtraction</strong> of two big integers</li>
        <li><strong>Multiplication</strong> of two big integers</li>
        <li><strong>Division</strong> of two big integers</li>
        <li><strong>Modulo</strong> of two big integers</li>
        <li><strong>Exponentiation</strong> (raise a big integer to a power)</li>
        <li><strong>Square root</strong> of a big integer (floor integer value)</li>
        <li><strong>Comparison</strong> between two big integers to check which is greater or smaller</li>
        <li><strong>Digit count</strong> of a big integer</li>
        <li><strong>Print</strong> a big integer</li>
        <li><strong>Convert</strong> a simple integer to a BigInt</li>
    </ul>

  <h2>Applications of BigInt</h2>
    <p>The <strong>BigInt</strong> data type can be applied in a variety of problems requiring the manipulation of large numbers:</p>
    <ul>
        <li>Calculating <strong>Fibonacci numbers</strong> for very large indices (up to 10,000 or even 100,000, though slower for very large numbers)</li>
        <li>Calculating <strong>Catalan numbers</strong> for large inputs</li>
        <li>Computing the <strong>Factorial</strong> of large integers (up to 1,000!)</li>
    </ul>

  <h2>Approach</h2>
    <p>The implementation of <strong>BigInt</strong> is based on the following key concepts:</p>

  <h3>1. Using Strings to Store Large Numbers</h3>
    <p>We store numbers in the form of characters (in reverse order for efficiency purposes) within C++ strings. This allows us to manage very large integers that can't be held in standard primitive types.</p>

  <h3>2. Basic Arithmetic Operations</h3>
    <p>For each arithmetic operation (addition, subtraction, multiplication, etc.), we apply basic mathematical concepts:</p>
    <ul>
        <li><strong>Addition/Subtraction</strong>: We add or subtract corresponding digits and handle carries or borrows by propagating them to the next digit until all digits are processed.</li>
        <li><strong>Multiplication</strong>: We multiply each digit of one number by the entire second number and then sum the results appropriately.</li>
    </ul>

  <h3>3. Operations on BigInt</h3>
    <p>The following operations are implemented for <strong>BigInt</strong>:</p>
    <ul>
        <li><strong>Defining BigIntegers</strong>: Create and initialize big integers.</li>
        <li><strong>Digit Count</strong>: Determine the number of digits in a BigInt.</li>
        <li><strong>Incrementation/Decrementation</strong>: Increment or decrement the value of a BigInt (post and pre-incrementation).</li>
        <li><strong>Arithmetic Operations</strong>: Add, subtract, multiply, divide, and calculate the modulo of two BigInts.</li>
        <li><strong>Square Root</strong>: Compute the floor value of the square root of a BigInt.</li>
        <li><strong>Exponentiation</strong>: Raise a BigInt to a power.</li>
    </ul>

  <h3>4. Special Operations</h3>
    <ul>
        <li><strong>Fibonacci Calculation</strong>: Compute Fibonacci numbers up to 10,000 (or higher, but slower for larger numbers).</li>
        <li><strong>Factorial Calculation</strong>: Compute factorials of numbers up to 1,000.</li>
        <li><strong>Catalan Number Calculation</strong>: Calculate Catalan numbers up to 1,000.</li>
        <li><strong>Comparison</strong>: Compare two BigInts to check which one is greater or smaller.</li>
    </ul>

  <h2>Example Usage</h2>
    <p>Here are a few examples of how to use the <strong>BigInt</strong> data type:</p>

  <h3>1. Defining and Printing BigInt</h3>
    <pre><code>BigInt num1 = "12345678901234567890";
BigInt num2 = 9876543210;
cout << "num1: " << num1 << endl;
cout << "num2: " << num2 << endl;</code></pre>

  <h3>2. Addition of BigInts</h3>
    <pre><code>BigInt sum = num1 + num2;
cout << "Sum: " << sum << endl;</code></pre>

  <h3>3. Factorial of a BigInt</h3>
    <pre><code>BigInt fact = factorial(100);
cout << "Factorial of 100: " << fact << endl;</code></pre>

  <h3>4. Fibonacci Calculation</h3>
    <pre><code>BigInt fib = fibonacci(10000);
cout << "Fibonacci(10000): " << fib << endl;</code></pre>

  <h2>Future Improvements</h2>
    <p>The current implementation of <strong>BigInt</strong> supports several basic operations and a few applications. Future improvements can include:</p>
    <ul>
        <li>Optimizing performance for extremely large numbers (e.g., greater than 100,000 digits).</li>
        <li>Implementing additional mathematical functions like logarithms, trigonometric functions, etc.</li>
        <li>Improving the efficiency of certain operations, especially for very large numbers.</li>
    </ul>

  <h2>Conclusion</h2>
    <p>The <strong>BigInt</strong> data type provides an easy-to-use and efficient solution for working with large integers in C/C++. With the ability to handle numbers far beyond the capacity of standard primitive types, <strong>BigInt</strong> enables developers to tackle problems in fields such as cryptography, large number computations, and more.</p>


