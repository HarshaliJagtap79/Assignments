# Assignments
//ShuffleArray
import java.util.Arrays;
import java.util.Random;
class ShuffleArray
{    public static void shuffle(int nums[])
    {
        for (int i = nums.length - 1; i >= 1; i--)
        {
            Random rand = new Random();
            int j = rand.nextInt(i + 1);
			swap_elements(nums, i, j);
        }
    }
    private static void swap_elements(int[] nums, int i, int j) 
	{
        int temp = nums[i];
        nums[i] = nums[j];
        nums[j] = temp;
    }
	 public static void main (String[] args)
    {
        int[] nums = { 1, 2, 3, 4, 5, 6 };
        System.out.println("Before  Array: "+Arrays.toString(nums));
        shuffle(nums);
		System.out.println("After Shuffled Array: "+Arrays.toString(nums));
    }
}
=====================================================================================================================
Roman Numbers
import java.util.*;
import java.io.*;
import java.lang.Math;
public class Roman {
   public static void main(String args[]) {
      Roman obj = new Roman();
      String inputRoman= "IX";
      System.out.println("The Integer value of given Roman number is: "+obj.romanToInt(inputRoman));
   } 
   int NumValue(char rom) {
      if (rom == 'I')
         return 1;
      if (rom == 'V')
         return 5;
      if (rom == 'X')
         return 10;
      if (rom == 'L')
         return 50;
      if (rom == 'C')
         return 100;
      if (rom == 'D')
         return 500;
      if (rom == 'M')
         return 1000;
      return -1;
   }
   int romanToInt(String str) {
      int sum = 0;
      for (int i=0; i<str.length(); i++) {
         int s1 = NumValue(str.charAt(i));
         if (i+1 <str.length()) {
           int s2 = NumValue(str.charAt(i+1));
           if (s1 >= s2) {
              sum = sum + s1;
           }
           else{
              sum = sum - s1;
           }
        }
        else {
           sum = sum + s1;
        } 
     }  
     return sum;
   }
} 
============================================================================================================
Pangram
class Pangram {
	static int size = 26;
	static boolean isLetter(char ch)
	{
		if (!Character.isLetter(ch))
			return false;
		return true;
	}
	static boolean allLetter(String str,int len)
	{
		str = str.toLowerCase();
		boolean[] present = new boolean[size];
		for (int i = 0; i < len; i++) 
			{
			if (isLetter(str.charAt(i))) {
				int letter = str.charAt(i) - 'a';
				present[letter] = true;
			}
}
	for (int i = 0; i < size; i++) 
		{			if (!present[i])
					return false;
		}			return true;
	}
	public static void main(String args[])
	{
		String str = "Abcdefghijklmnopqrstuvwxyz";
		int len = str.length();
		if (allLetter(str, len))
			System.out.println("The Given String is Pangram!!!");
		else
			System.out.println("The Given String is Not a Pangram!!!");
	}
}
=========================================================================================================
Reversed String
function reverseString(str) {
    let newString = "";
    for (let i = str.length - 1; i >= 0; i--) {
        newString += str[i];
    }
    return newString;
}
console.log(`Reversed string is : ${reverseString('Harshali')}`)
=========================================================================================================
Descending Order
const arr1 = [24.6,23.7,18.9,76.5]; 
const arr2 = [54,23,12,97,100]; 

function arrSort(arr) { 
	arr.sort((a,b)=>b-a); 
	return arr; 
} 

console.log(arrSort(arr1)); 
console.log(arrSort(arr2));
========================================================================================================
Calculator Using Html,CSS and Javascript
<!DOCTYPE html>
<html lang="en">
<head>
   <link rel="stylesheet" href="style.css">
   <title>Calculator with HTML, CSS and Javascript</title>
</head>
<body>
   <div class="main">
      <input type="text" id = 'res'>
      <div class="btn">
         <input type="button" value = 'C' onclick = "Clear()">
         <input type="button" value = '%' onclick = "Solve('%')">
         <input type="button" value = '←' onclick ="Back('←')">
         <input type="button" value = '/' onclick = "Solve('/')">
         <br>
         <input type="button" value = '7' onclick = "Solve('7')">
         <input type="button" value = '8' onclick = "Solve('8')">
         <input type="button" value = '9' onclick = "Solve('9')">
         <input type="button" value = 'x' onclick = "Solve('*')">
         <br>
         <input type="button" value = '4' onclick = "Solve('4')">
         <input type="button" value = '5' onclick = "Solve('5')">
         <input type="button" value = '6' onclick = "Solve('6')">
         <input type="button" value = '-' onclick = "Solve('-')">
         <br>
         <input type="button" value = '1' onclick = "Solve('1')">
         <input type="button" value = '2' onclick = "Solve('2')">
         <input type="button" value = '3' onclick = "Solve('3')">
         <input type="button" value = '+' onclick = "Solve('+')">
         <br>
         <input type="button" value = '00'onclick = "Solve('00')">
         <input type="button" value = '0' onclick = "Solve('0')">
         <input type="button" value = '.' onclick = "Solve('.')">
         <input type="button" value = '=' onclick = "Result()">
      </div>
   </div>
   <script src = 'script.js' ></script>
</body>
</html>
Html Code
======================================================================================================
Css Code
*{
    padding: 0;
    margin: 0;
    font-family: 'poppins', sans-serif;
 }
 body{
    background-color: #495250;
    display: grid;
    height: 100vh;
    place-items: center;
 }
 .main{
    width: 400px;
    height: 450px;
    background-color: white;
    position: absolute;
    border: 5px solid black;
    border-radius: 6px; 
 }
 .main input[type='text'] {
    width: 88%;
    position: relative;
    height: 80px;
    top: 5px;
    text-align: right;
    padding: 3px 6px;
    outline: none;
    font-size: 40px;
    border: 5px solid black;
    display: flex;
    margin: auto;
    border-radius: 6px;
    color: black;
 }
 .btn input[type='button']{
    width:90px;
    padding: 2px;
    margin: 2px 0px;
    position: relative;
    left: 13px;
    top: 20px;
    height: 60px;
    cursor: pointer;
    font-size: 18px;
    transition: 0.5s;
    background-color: #495250;
    border-radius: 6px;
    color: white;
 }
 .btn input[type='button']:hover{
    background-color: black;
    color: white;
 }
 =================================================================================================
 Js Code
 function Solve(val) {
    var v = document.getElementById('res');
    v.value += val;
 }
 function Result() {
    var num1 = document.getElementById('res').value;
    var num2 = eval(num1);
    document.getElementById('res').value = num2;
 }
 function Clear() {
    var inp = document.getElementById('res');
    inp.value = '';
 }
 function Back() {
    var ev = document.getElementById('res');
    ev.value = ev.value.slice(0,-1);
 }
 =================================================================================================
 Survey Form
 <!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>
		Build a Survey Form using HTML and CSS
	</title>

	<style>

		/* Styling the Body element i.e. Color, 
		Font, Alignment */ 
		body {
			background-color: green;
			font-family: Verdana;
			text-align: center;
		}

		/* Styling the Form (Color, Padding, Shadow) */
		form {
			background-color: #fff;
			max-width: 500px;
			margin: 50px auto;
			padding: 30px 20px;
			box-shadow: 2px 5px 10px rgba(0, 0, 0, 0.5);
		}

		/* Styling form-control Class */
		.form-control {
			text-align: left;
			margin-bottom: 25px;
		}

		/* Styling form-control Label */ 
		.form-control label {
			display: block;
			margin-bottom: 10px;
		}

		/* Styling form-control input, 
		select, textarea */
		.form-control input,
		.form-control select,
		.form-control textarea {
			border: 1px solid #777;
			border-radius: 2px;
			font-family: inherit;
			padding: 10px;
			display: block;
			width: 95%;
		}

		/* Styling form-control Radio 
		button and Checkbox */
		.form-control input[type="radio"],
		.form-control input[type="checkbox"] {
			display: inline-block;
			width: auto;
		}

		/* Styling Button */
		button {
			background-color: #05c46b;
			border: 1px solid #777;
			border-radius: 2px;
			font-family: inherit;
			font-size: 21px;
			display: block;
			width: 100%;
			margin-top: 50px;
			margin-bottom: 20px;
		}
	</style>
</head>

<body>
	<h2>Survey Form</h2>

	<!-- Create Form -->
	<form id="form">

		<!-- Details -->
		<div class="form-control">
			<label for="name" id="label-name">
				First Name
			</label>

			<!-- Input Type Text -->
			<input type="text"
				id="name"
				placeholder="Enter your First name" />
		</div>

        <div class="form-control">
			<label for="name" id="label-name">
				Last Name
			</label>

			<!-- Input Type Text -->
			<input type="text"
				id="name"
				placeholder="Enter your Last name" />
		</div>


		<div class="form-control">
			<label for="email" id="label-email">
			Email
			</label>

			<!-- Input Type Email-->
			<input type="email"
				id="email"
				placeholder="Enter your Valid email" />
		</div>

		<div class="form-control">
			<label for="age" id="label-age">
			Age
			</label>

			<!-- Input Type Text -->
			<input type="text"
				id="age"
				placeholder="Enter your age" />
		</div>

		<div class="form-control">
			<label for="role" id="label-role">
				Which option best describes you?
			</label>
			
			<!-- Dropdown options -->
			<select name="role" id="role">
				<option value="student">Student</option>
				<option value="intern">Intern</option>
				<option value="professional">
					Professional
				</option>
				<option value="other">Other</option>
			</select>
		</div>

		<div class="form-control">
			<label>
				Would you recommend GeeksforGeeks 
				to a friend?
			</label>

			<!-- Input Type Radio Button -->
			<label for="recommed-1">
				<input type="radio"
					id="recommed-1"
					name="recommed">Yes</input>
			</label>
			<label for="recommed-2">
				<input type="radio"
					id="recommed-2"
					name="recommed">No</input>
			</label>
			<label for="recommed-3">
				<input type="radio"
					id="recommed-3"
					name="recommed">Maybe</input>
			</label>
		</div>

		<div class="form-control">
			<label>Languages and Frameworks known 
				<small>(Check all that apply)</small>
			</label>
			<!-- Input Type Checkbox -->
			<label for="inp-1">
				<input type="checkbox"
					name="inp">C</input></label>
			<label for="inp-2">
				<input type="checkbox"
					name="inp">C++</input></label>
			<label for="inp-3">
				<input type="checkbox"
					name="inp">C#</input></label>
			<label for="inp-4">
				<input type="checkbox"
					name="inp">Java</input></label>
			<label for="inp-5">
				<input type="checkbox"
					name="inp">Python</input></label>
			<label for="inp-6">
				<input type="checkbox"
					name="inp">JavaScript</input></label>
			<label for="inp-7">
				<input type="checkbox"
					name="inp">React</input></label>
			<label for="inp-7">
				<input type="checkbox"
					name="inp">Angular</input></label>
			<label for="inp-7">
				<input type="checkbox"
					name="inp">Django</input></label>
			<label for="inp-7">
				<input type="checkbox"
					name="inp">Spring</input></label>
		</div>

		<div class="form-control">
			<label for="comment">
				Any comments or suggestions
			</label>

			<!-- multi-line text input control -->
			<textarea name="comment" id="comment"
				placeholder="Enter your comment here">
			</textarea>
		</div>

		<!-- Multi-line Text Input Control -->
		<button type="submit" value="submit">
			Submit
		</button>
	</form>
</body>
</html>



