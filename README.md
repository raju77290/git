1.	Check Sum of Odd Digits
MAIN:
import java.util.*;
public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in);
int n=s.nextInt();
int r=UserMainCode.checkSum(n);
if(r==1)
{

}
else
{

}
 System.out.println("The sum of odd digits are odd");
System.out.println("The sum of odd digits are even");
 s.close();
}
}
USERMAINCODE:
public class UserMainCode {
public static int checkSum(int n)
{
int  n1; int sum=0; int r; while(n!=0)
{
n1=n%10;
if(n1%2!=0)
{
sum=sum+n1; 
}
n=n/10;
}
if(sum%2==0)
{

}
else
{

} 
r=-1;
r=1;
 return r;
}
}
2.Number Validation

MAIN:
import java.util.*;
public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String number=s.next();
int r=UserMainCode.validateNumber(number);
if(r==1)
{
System.out.println("Valid number format“);
}
 else
{

}
 
System.out.println("Invalid number format");
 s.close();
}

}

USERMAINCODE:
import java.util.*;
public class UserMainCode {
public static int validateNumber(String number)
{
int b;
if(number.matches("[0-9]{3}[-]{1}[0-9]{3}[-]{1}[0-9]{4}"))
{
 

}
else
{

}
 b=1;
b=0;
 return b;
}
}

3.	Sum of Squares of Even Digits
MAIN:
import java.util.*;
public class Main {
public static void main(String[] args)
{
 Scanner s=new Scanner(System.in);
int n=s.nextInt(); System.out.println(UserMainCode.sumOfSquaresOfEvenDigits(n)); s.close();
}
}

USERMAINCODE:
public class UserMainCode {
public static int sumOfSquaresOfEvenDigits(int n)
{
int n1=0; int sum=0; while(n!=0)
{
n1=n%10;
if(n1%2==0)
{
sum+=n1*n1;
}
n=n/10;
}
return sum;
}
}
4.	Fetching Middle Characters from String 
MAIN:
import java.util.*;
public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String str=s.nextLine();
System.out.println(UserMainCode.getMiddleChars(str)); s.close();
}
}
USERMAINCODE:
import java.util.*;
public class UserMainCode {
public static String getMiddleChars(String str)
{
StringBuffer sb=new StringBuffer();
if(str.length()%2==0)
{
sb.append(str.substring((str.length()/2)-1,(str.length()/2)+1));
}
return sb.toString();
}
}
5.	Check Characters in a String
MAIN:
import java.util.*;
public class main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String input=s.nextLine();
int r=UserMainCode.checkCharacters(input);
if(r==1)
{

}
else
{

}
 System.out.println("Valid");
System.out.println("Invalid");
 s.close();
}
}
USERMAINCODE:
import java.util.*;
public class UserMainCode {
public static int checkCharacters(String input)
{
int r;
StringTokenizer t = new StringTokenizer(input," "); String s = t.nextToken();
String s1 =s ;
while(t.hasMoreTokens())
{
s1 = t.nextToken();
}
if(s.charAt(0) == s1.charAt(s1.length()-1)) r=1;
else
r=0;
return r;
}
}
6.	Forming New Word from a String
MAIN:
import java.util.*;
public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String s1=s.nextLine();
int n1=s.nextInt(); System.out.println(UserMainCode.formNewWord(s1,n1)); s.close();
}
}
USERMAINCODE:
import java.util.*;
public class UserMainCode {
public static String formNewWord(String s1,int n)
{
String s = new String();
if(s1.length()>n)
{
s = s1.substring(0,n) + s1.substring(s1.length()-n, s1.length());
return s;
}
else
return null;
}
}
 7.	Reversing a Number
MAIN:
import java.util.*;
public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in);
int n=s.nextInt(); System.out.println(UserMainCode.reverseNumber(n)); s.close();
}
}

USERMAINCODE:
public class UserMainCode {
public static int reverseNumber(int n)
{
int a,r=0;
while(n!=0)
{
a=n%10;
r=r*10+a; n=n/10;
}
return r;
}
}

8.	Array List Sorting and Merging
Main:
import java.util.*;
public class Main {
public static void main(String[] args) 
{
Scanner s=new  Scanner(System.in); ArrayList<Integer> list1=new ArrayList<Integer>(); ArrayList<Integer> list2=new ArrayList<Integer>(); ArrayList<Integer> newlist=new ArrayList<Integer>(); for (int i = 0; i < 5; i++)
{
list1.add(s.nextInt());
}
for (int i = 0; i < 5; i++)
{
list2.add(s.nextInt());
}
newlist=UserMainCode.sortMergedArraylist(list1,list2);
for (int i = 0; i < 3; i++)
{
System.out.println(newlist.get(i));
}
s.close();
}
}
UERMAINCODE:
import java.util.*;
public class UserMainCode {
public static ArrayList<Integer> sortMergedArraylist(ArrayList<Integer> list1,ArrayList<Integer> list2)
{
list1.addAll(list2); Collections.sort(list1);
ArrayList<Integer> ans=new ArrayList<Integer>(); ans.add(list1.get(2));
ans.add(list1.get(6));
ans.add(list1.get(8));
return ans;
}
}
9.	Validating Date Format
Main:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in); String s1=sc.nextLine();
int b=UserMainCode.ValidateDate(s1);
if(b==1){
System.out.println("Valid date format");
}
else{

}
 
System.out.println("Invalid date format"); 
sc.close();
}}
UserMainCode:
import  java.util.*; import  java.text.*; public class UserMainCode{
public static int ValidateDate(String s1) { if(s1.matches("[0-9]{2}[/]{1}[0-9]{2}[/]{1}[0-9]{4}"))
{
SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); sdf.setLenient(false);
try {
Date d1=sdf.parse(s1); return 1;
} catch (ParseException e) { return -1;
}
}
else{
return -1;}}}

10.	Validate Time
Main:
import java.util.*;
public class Main{
public static void main(String []args){ Scanner sc=new Scanner(System.in); String str=sc.nextLine();
int b=UserMainCode.ValidateTime(str);
if(b==1){
System.out.println("Valid time"); 
}
else{

} 

System.out.println("Invalid time");
 sc.close();
}}
UserMainCode:
import  java.text.*; import  java.util.*; public class UserMainCode{
public static int ValidateTime(String str){ StringTokenizer st=new StringTokenizer(str,":"); if(st.countTokens()==3)
{
SimpleDateFormat sdf1 = new SimpleDateFormat("h:mm:ss a"); sdf1.setLenient(false);
try
{
Date d2=sdf1.parse(str); return 1;
}
catch(Exception e)
{
return -1;
}}
else
{
SimpleDateFormat sdf = new SimpleDateFormat("h:mm a"); sdf.setLenient(false);
try
{
Date d1=sdf.parse(str); return 1;
} 
catch(Exception e){
return -1;
}}}}

11.	String Encryption
Main:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
String s1=s.next(); System.out.println(UserMainCode.encrypt(s1)); s.close();
}
}
UserMainCode:
public class UserMainCode{
public static String encrypt(String s1) { StringBuffer sb=new StringBuffer(); for(int i=0;i<s1.length();i++){
char c=s1.charAt(i); if(i%2==0){ if(c==122) if((c==122)&&(i==0)){ c='A';}
else
c=(char) (c-25);
else{
 c=(char) (c+1);}
sb.append(c);} else sb.append(c);}
return sb.toString();
}}
12.	Password Validation
Main:
import java.util.*;
public class Main {
public static void main(String[] args){ Scanner s=new Scanner(System.in);
String password=s.next();
int b=UserMainCode.ValidatePassword(password);
if(b==1){
System.out.println("Valid Password");
}
else{
System.out.println("Invalid Password");
}
s.close();
}}
UserMainCode:
public class UserMainCode{
public static int ValidatePassword(String password){ if(password.matches(".*[0-9]{1,}.*") && password.matches(".*[@#$]{1,}.*") && password.length()>=6 && password.length()<=20)
{
 return 1;
}
else
{
return -1;
}}}

13.	Removing vowels from String
Main:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.nextLine();
System.out.println(UserMainCode.removeEvenVowels(s1)); s.close();
}}

UserMainCode:
public class UserMainCode{
public static String removeEvenVowels(String s1) { StringBuffer sb1=new StringBuffer();
for(int i=0;i<s1.length();i++)
if((i%2)==0)
sb1.append(s1.charAt(i));
else if((i%2)!=0)
if(s1.charAt(i)!='a' && s1.charAt(i)!='e' && s1.charAt(i)!='i' && s1.charAt(i)!='o' && s1.charAt(i)!='u') if(s1.charAt(i)!='A' && s1.charAt(i)!='E' && s1.charAt(i)!='I' && s1.charAt(i)!='O' && s1.charAt(i)!='U') sb1.append(s1.charAt(i));
return sb1.toString();
}}
 
14.	Sum of Powers of elements in an array
Main:
import java.util.Scanner;
public class Main{
public static void main(String args[]){ Scanner sc=new Scanner(System.in);
int n=sc.nextInt(); int a[]=new int[n]; for(int i=0;i<n;i++)
{
a[i]=sc.nextInt();
}
System.out.println(UserMainCode.getSumOfPower(n,a)); sc.close();
}}
UserMainCode:
public class UserMainCode{
public static int getSumOfPower(int n,int[]a)
{{
int sum=0;
for(int i=0;i<n;i++)
 sum=(int)(sum+Math.pow(a[i], i));
return sum;
}}}

15.	Difference between largest and smallest elements in an array
Main:
import java.util.*;
public class Main {
public static void main(String args[]){ Scanner sc=new Scanner(System.in); int n=sc.nextInt();
int a[]=new int[n]; for(int i=0;i<n;i++)
{
a[i]=sc.nextInt();
}
System.out.println(UserMainCode.getBigDiff(a,n)); sc.close(); 
}}
UserMainCode:
import java.util.*;
public class UserMainCode{
public static int getBigDiff(int [] a,int n)
{
Arrays.sort(a);
int n1=a[a.length-1]-a[0];
return n1;
}}

16.	Find the element position in a reversed string array
Main:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in);
int fr=sc.nextInt();
 String a[]=new String[fr];
for(int i=0;i<fr;i++)
{
a[i]=sc.next();
}
String ba=sc.next(); UserMainCode.getElementPosition(a,ba); sc.close();
}}

UserMainCode:
import java.util.*;
public class UserMainCode{
public static void getElementPosition(String[] a, String b) { ArrayList<String>al=new ArrayList<String>();
for(int i=0;i<a.length;i++)
{
al.add(a[i]);
}
Collections.sort(al); Collections.reverse(al); for(int i=0;i<al.size();i++)
{
if(b.equals(al.get(i)))
{
System.out.println(i+1);
}}}}

17.	generate the series

Main
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
int n=s.nextInt(); System.out.println(UserMainCode.addSeries(n)); s.close();
}
}
UserMainCode
import java.util.ArrayList;
import java.util.List;
public class UserMainCode {
public static int addSeries(int n){ List<Integer> l1=new ArrayList<Integer>(); for(int i=1;i<=n;i++)
if(i%2!=0) l1.add(i);
int n1=l1.get(0);
for(int i=1;i<l1.size();i++)
if(i%2!=0) n1=n1+l1.get(i); else
n1=n1-l1.get(i);
return n1;
}
}
18.	Calculate Electricity Bill
Main
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String input1=s.next();
String input2=s.next();
int input3=s.nextInt();
 System.out.println(UserMainCode.calculateElectricityBill(input1,input2,inpu
t3));
s.close();
}
}
UserMainCode
public class UserMainCode {
public static int calculateElectricityBill(String input1, String input2,
int input3)
{
int n1=Integer.parseInt(input1.substring(5, input1.length())); int n2=Integer.parseInt(input2.substring(5, input2.length())); int n=Math.abs((n2-n1)*input3);
return n;
}
}
19.	Sum of Digits in a String
Main
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.next(); UserMainCode.sumOfDigits(s1);  s.close();
}
}
UserMainCode
public class UserMainCode {
public static void sumOfDigits(String s1) {
int sum=0;
for(int i=0;i<s1.length();i++)
{
 char a=s1.charAt(i);
if(Character.isDigit(a))
{
int b=Integer.parseInt(String.valueOf(a)); sum=sum+b;
}
}
if(sum==0)
{
System.out.println(-1);
}
else
System.out.println(sum);
}
}
20.	String Concatenation
Main
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.next();
String s2=s.next(); UserMainCode.concatstring(s1,s2); s.close();
 }
} 
UserMainCode
public class UserMainCode {
public static void concatstring(String s1, String s2) { StringBuffer sb=new StringBuffer();
int l1=s1.length(); int l2=s2.length(); if(l1==l2)
{
sb.append(s1).append(s2);
}
else if(l1>l2)
{
sb.append(s1.substring(s1.length()- s2.length(),s1.length())).append(s2);
}
else if(l1<l2)
{
sb.append(s1).append(s2.substring(s2.length()- s1.length(),s2.length()));
}
System.out.println(sb);
}
}
21.	Color Code
Main
import java.util.*;
public class Main { 
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.next();
int b=UserMainCode.validateColorCode(s1);
if(b==1) System.out.println("Valid"); else System.out.println("Invalid"); s.close();
}
}
UserMainCode
public class UserMainCode {
public static int validateColorCode(String s1) {
int b=0,b1=0;
String s2=s1.substring(1,s1.length()); if(s1.length()==7) if(s1.charAt(0)=='#')
b1=1;
if(b1==1){/*for(int i=0;i<s2.length();i++){
char c=s2.charAt(i); if(c!='#'){*/if(s2.matches("[A-F0-9]{1,}"))
b=1;
 else
b=-1;
//break;
}
return b;
}
}
22.	Three Digits
Main
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.next();
int b=UserMainCode.validatestrings(s1);
if(b==1){
System.out.println("Valid");} else System.out.println("Invalid"); s.close();
}
}
UserMainCode
public class UserMainCode {
public static int validatestrings(String s1) {
int res=0;
if(s1.matches("(CTS)[-]{1}[0-9]{3}"))
{
res=1;
}
else
 res=-1;
return res;
}
}
23.	Removing Keys from HashMap
Main
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in);
int s=sc.nextInt();
HashMap<Integer, String>hm=new HashMap<Integer, String>();
for(int i=0;i<s;i++){
hm.put((sc.nextInt()),(sc.next()));
}
System.out.println(UserMainCode.sizeOfResultandHashMap(hm));
sc.close();
} }
UserMainCode
import java.util.HashMap;
import java.util.Iterator;
public class UserMainCode {
public static int sizeOfResultandHashMap(HashMap<Integer, String> hm) {
int count=0;
Iterator<Integer>itr=hm.keySet().iterator();
while(itr.hasNext())
{
int n=itr.next();
if(n%4!=0)
{
count++;
}
}
return count;
}
}
24.	Largest Element

Main
import java.util.*;
public class Main { 
public static void main(String[] args) { Scanner s=new Scanner(System.in); int n=s.nextInt();
int a[]=new int[n]; for(int i=0;i<n;i++){
a[i]=s.nextInt();
}
System.out.println(UserMainCode.checkLargestAmongCorner(a)); s.close();
}
}

UserMainCode
public class UserMainCode {
public static int checkLargestAmongCorner(int []a)
{
int max=0;
int x,y,z;
x=a[0];
y=a[a.length/2]; z=a[a.length-1]; if(x>y && x>z) max=x;
else if(y>x && y>z) max=y;
 else if(z>x && z>y) max=z;
return max;
}
}
25.	nCr

Main

import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
int n=s.nextInt();
int r=s.nextInt(); System.out.println(UserMainCode.calculateNcr(n,r));
}
}
UserMainCode
public class UserMainCode {
public static int calculateNcr(int n, int r) {
int fact=1,fact1=1,fact2=1;
for(int i=1;i<=n;i++)
{
fact=fact*i;
}
//System.out.println(fact);
for(int i=1;i<=r;i++)
{
fact1=fact1*i; 
}
//System.out.println(fact1);
for(int i=1;i<=(n-r);i++)
{
fact2=fact2*i;
}
//System.out.println(fact2); int res=fact/(fact1*fact2); return res;
}
}
26.	Sum of Common Elements

Main
import java.util.Scanner;
public class Main {
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in);

int n=sc.nextInt(); int m=sc.nextInt(); int[] a=new int[n]; int[] b=new int[m]; for(int i=0;i<n;i++){ a[i]=sc.nextInt();} for(int i=0;i<m;i++){ b[i]=sc.nextInt();}
int u=UserMainCode.getSumOfIntersection (a,b,n,m);
if(u==-1)System.out.println("No common elements");
else
System.out.println(u); sc.close();
}}
UserMainCode
public class UserMainCode {
 public static int getSumOfIntersection(int a[],int b[],int n,int m)
{
int sum=0;
for(int i=0;i<a.length;i++)
{
for(int j=0;j<b.length;j++)
{
if(a[i]==b[j]) sum=sum+a[i];
}}
if(sum==0) return -1; else  return sum;
}
}
27.	Validating Input Password
Main
import java.util.*;
public class Main{
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in); String a=sc.next();
int e=UserMainCode.validatePassword(a);
if(e==1){ System.out.println("Valid");
}
else
{
System.out.println("Invalid");
}
sc.close();
}}
UserMainCode
public class UserMainCode {
public static int validatePassword(String a){
int d=0;
if(a.length()>=8){
if(a.contains("#") || a.contains("@") || a.contains("_"))
{
char c= a.charAt(0);
//System.out.println(c);
if(Character.isAlphabetic(c))
{
char dd=a.charAt(a.length()-1);
//System.out.println(dd);
if((Character.isAlphabetic(dd))||(Character.isDigit(dd)))
{
if(a.matches(".*[0-9]{1,}.*")||a.matches(".*[a-zA-Z]{1,}.*")){ d=1;
}
}
}
 }
}
else
d=-1;
return d;
}}
28.	iD Validation
Main
import java.util.*;
public class Main3 {
public static void main(String[] args) { Scanner sc=new Scanner(System.in);
String s1=sc.next(); String s2=sc.next();
boolean b=UserMainCode3.validateIDLocations(s1,s2);
if(b==true) System.out.println("Valid id"); else
System.out.println("Invalid id");
sc.close();
 }
}
UserMainCode
import java.util.StringTokenizer;
public class UserMainCode3 {
public static boolean validateIDLocations(String s1, String s2) { String s3=s2.substring(0, 3);
boolean b=false;
StringTokenizer t=new StringTokenizer(s1,"-"); String s4=t.nextToken();
String s5=t.nextToken(); String s6=t.nextToken();
if(s4.equals("CTS") && s5.equals(s3) && s6.matches("[0-9]{4}")) b=true;
else{ b=false;} return b;
}
}
29.	Remove Elements
Main
import java.util.*;
public class Main
{
public static void main(String[] args)
{
Scanner sc=new  Scanner(System.in); int n=Integer.parseInt(sc.nextLine()); String[] a=new String[n];
for(int i=0;i<n;i++) a[i]=sc.nextLine();
int m=Integer.parseInt(sc.nextLine()); System.out.println(UserMainCode.removeElements(a,m)); sc.close();
}
}
UserMainCode
public class UserMainCode {
public static int removeElements(String[] a,int m){
int u=a.length;
for(int i=0;i<a.length;i++)
{
if(a[i].length()==m) u--;
}
return u;
}
}
 30.	Find the difference between Dates in months
Main
import java.text.*;
import java.util.*;
public class Main {
public static void main(String[] args) throws ParseException { Scanner sc=new Scanner(System.in);
String s1=sc.next(); String s2=sc.next();
System.out.println(UserMainCode.getMonthDifference(s1,s2)); sc.close();
}}
UserMainCode
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.Calendar;
import java.util.Date;
public class UserMainCode {
public static int getMonthDifference(String s1, String s2) throws
ParseException {
SimpleDateFormat sdf=new SimpleDateFormat("yyyy-MM-dd"); Date d1=sdf.parse(s1);
Date d2=sdf.parse(s2);
Calendar cal=Calendar.getInstance();
 cal.setTime(d1);
int months1=cal.get(Calendar.MONTH); int year1=cal.get(Calendar.YEAR); cal.setTime(d2);
int months2=cal.get(Calendar.MONTH);
int year2=cal.get(Calendar.YEAR);
int n=((year2-year1)*12)+(months2-months1);
return n;
}
}
31.	Sum of cubes and squares of elements in an array
Main
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in); int n=sc.nextInt();
int a[]=new int[n]; for(int i=0;i<n;i++){
a[i]=sc.nextInt();
}
System.out.println(UserMainCode.addEvenOdd(a)); sc.close();
}
 }
UserMainCode
public class UserMainCode6 {
public static int addEvenOdd(int[] a) {
int n1=0,n2=0;
for(int i=0;i<a.length;i++) if(a[i]%2==0) n1+=(a[i]*a[i]);
else n2+=(a[i]*a[i]*a[i]); return n1+n2;
}
}
32.	IP Validator
Main
import java.util.*;
public class Main7 {
public static void main(String[] args) { Scanner sc=new Scanner(System.in);
String ipAddress=sc.next();
boolean b=UserMainCode7.validateIpAddress(ipAddress);
if(b==true) System.out.println("Valid"); else System.out.println("Invalid"); sc.close();
}} 
UserMainCode
import java.util.StringTokenizer;
public class UserMainCode7 {
public static boolean validateIpAddress(String ipAddress) {
boolean b1=false;
StringTokenizer t=new StringTokenizer(ipAddress,".");
int a=Integer.parseInt(t.nextToken()); int b=Integer.parseInt(t.nextToken()); int c=Integer.parseInt(t.nextToken()); int d=Integer.parseInt(t.nextToken());
if((a>=0 && a<=255)&&(b>=0 && b<=255)&&(c>=0 && c<=255)&&(d>=0 && d<=255))
b1=true;
return b1;
}
}
33.	Difference between two dates in days

Main
import java.text.ParseException;
import java.util.*;
public class Main {
public static void main(String[] args) throws ParseException
 {
Scanner s=new Scanner(System.in); String s1=s.nextLine();
String s2=s.nextLine();
int output=UserMainCode.getDateDifference(s1,s2); System.out.println(output);
s.close();
}
}
UserMainCode
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.*;
public class UserMainCode {
public static int getDateDifference(String s1,String s2) throws ParseException
{
SimpleDateFormat sd=new SimpleDateFormat("yyyy-MM-dd"); Date d=sd.parse(s1);
Calendar c=Calendar.getInstance(); c.setTime(d);
long d1=c.getTimeInMillis(); d=sd.parse(s2); c.setTime(d);
long d2=c.getTimeInMillis();
int n=Math.abs((int) ((d1-d2)/(1000*3600*24)));
return n;
}} 
34.	File Extension
Main
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); System.out.println("enter the string"); String s1=s.nextLine();
String output=UserMainCode.fileIdentifier(s1); System.out.println(output);
 s.close();
}
}
UserMainCode
import java.util.*;
public class UserMainCode {
public static String fileIdentifier(String s1)
{
StringTokenizer t=new StringTokenizer(s1,"."); t.nextToken();
String s2=t.nextToken();
return s2;
}
}
35.	Find common characters and unique characters in string
Main
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in); String s1=sc.nextLine();
String s2=sc.nextLine();
StringBuffer sb1=new StringBuffer(s1.replace(" ",""));
 StringBuffer sb2=new StringBuffer(s2.replace(" ","")); int output=UserMainCode.commonChars(s1,s2,sb1,sb2); System.out.println(output);
sc.close();
}
}
UserMainCode
import java.util.*;
public class UserMainCode {
public static int commonChars(String s1,String s2,StringBuffer sb1,StringBuffer sb2) {
for(int i=0;i<sb1.length();i++){
int c=0;
for(int j=i+1;j<sb1.length();j++){ if(sb1.charAt(i)==sb1.charAt(j)){ sb1.deleteCharAt(j);
c++;
}
}
if(c>=1){ sb1.deleteCharAt(i);
}
}
for(int i=0;i<sb2.length();i++){
int c=0;
for(int j=i+1;j<sb2.length();j++){ if(sb2.charAt(i)==sb2.charAt(j)){ sb2.deleteCharAt(j);
 c++;
}
}
if(c>=1){ sb2.deleteCharAt(i);
}
}
int count=0;
for(int i=0;i<sb1.length();i++){ for(int j=0;j<sb2.length();j++){ if(sb1.charAt(i)==sb2.charAt(j)){ count++;
}
}
}
return (count);
}
}
36.	Initial Format
Main
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.nextLine();
String output=UserMainCode.nameFormatter(s1); System.out.println(output);
s.close();
}
}
UserMainCode
import java.util.*;
public class UserMainCode {
public static String nameFormatter(String s1) { StringBuffer sb=new StringBuffer(); StringTokenizer st=new StringTokenizer(s1," "); String s2=st.nextToken();
String s3=st.nextToken();
 sb.append(s3).append(","); sb.append(s2.substring(0,1).toUpperCase()); return sb.toString();
}
}
37.	Character cleaning
Main
import java.util.*; public class Main {
 public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.nextLine();
String c=s.nextLine();
String output=UserMainCode.removeCharacter(s1,c); System.out.println(output);
}
}
UserMainCode
import java.util.*;
public class UserMainCode {
public static String removeCharacter(String s1,String c)
{
String d=s1.replace(c,"");
return d;
}
}
38.	Vowel Check
Main
import java.util.*;
public class User {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.nextLine();
String s2=s1.toLowerCase();
int output=UserMainCode.getVowels(s2);
//System.out.println(output);
if(output==1)
{
System.out.println("yes");
}
else
System.out.println("no");
 s.close();
}
}
UserMainCode
import java.util.*;
public class UserMainCode {
public static int getVowels(String s2) {
if(s2.contains("a") && s2.contains("e") && s2.contains("i") && s2.contains("o") && s2.contains("u") )
{
return 1;
}
else return -1;
}
}
39.	Swap Characters
Main
import java.util.*;
public class Main

{
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.nextLine();
String output=UserMainCode.swapCharacter(s1); System.out.println(output);
s.close();
}
}
UserMainCode
import java.util.*;
public class UserMainCode {
public static String swapCharacter(String s1)
{
 StringBuffer sb=new StringBuffer();
int l=s1.length();
if(l%2==0)
{
for(int i=0;i<s1.length()-1;i=i+2)
{
char a=s1.charAt(i); char b=s1.charAt(i+1); sb.append(b).append(a);
}
return sb.toString();
}
else
{
for(int i = 0;i<s1.length()-1;i=i+2)
{
char a=s1.charAt(i); char b=s1.charAt(i+1); sb.append(b).append(a);
}
sb.append(s1.charAt(l-1));
return sb.toString();
}
}
}
40.	Average of Elements in Hashmap
Main
import java.util.HashMap; import java.util.Scanner; public class Main {
public static void main(String []args){ Scanner sc=new Scanner(System.in);
int s=sc.nextInt();
HashMap<Integer,Float>hm=new HashMap<Integer,Float>();
for(int i=0;i<s;i++)
{
int r=sc.nextInt(); Float j=sc.nextFloat(); hm.put(r,j);
}
System.out.println(UserMainCode.display(hm)); sc.close();
 }
}
UserMainCode
import java.text.DecimalFormat;
import java.util.*;
public class UserMainCode
{
public static String display(HashMap<Integer,Float>hm)
{

float sum=0;

int count=0;

DecimalFormat df=new DecimalFormat("#.00"); Iterator<Integer> it=hm.keySet().iterator(); while(it.hasNext())
{

int y=it.next();

if(y%2==0)

{

sum=(float) (sum+hm.get(y)); count++;
}}

float d=sum/count;

return df.format(d);

}

}
 

41.	Calculate Average – Hash Map

Main

import java.util.*; import java.text.*; public class Main {
public static void main(String[] arg)
{
HashMap<Integer,Double> hm=new HashMap<Integer,Double>(); Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
for(int i=0;i<n;i++)
{
int a=sc.nextInt(); double s=sc.nextDouble(); hm.put(a,s);
}
System.out.println(UserMaincode.dis(hm));}}

UserMainCode

class UserMaincode
{
public static double dis(HashMap<Integer,Double> h1)
 
{
double avg=0.0,sum=0.0;
int k=0;
for(Map.Entry m:h1.entrySet())
{
int a=(Integer)m.getKey();
if(a%2!=0)
{
Double d=(Double) m.getValue(); sum=sum+d;
k++;
}
}
avg = (double)sum/k;
DecimalFormat df = new DecimalFormat(".##"); String b1 = df.format(avg);
double b = Double.parseDouble(b1);
return b;}


42.	Count Sequential Characters Main
import java.util.*;
import java.text.*;

public class Main {
public static void main(String[] args) { Scanner sc=new Scanner (System.in);
String input1=sc.next(); System.out.println(UserMainCode.consecutiveRepeatitionOfChar(input1));
 
}
}

UserMainCode

class UserMainCode
{

public static int consecutiveRepeatitionOfChar(String input1)
{
int c=0;
int n=0;
for(int i=0;i<input1.length()-1;i++){ if(input1.charAt(i)==input1.charAt(i+1)) n++;
else
n=0;
if(n==2) c++; }
return c;
}
}

43.	Length of the Largest Chunk
Main
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in); String s1=sc.nextLine();
System.out.println(UserMainCode.largestChunk(s1));
 
}
}

UserMaincode
class UserMainCode
{
public static int largestChunk(String s1) {
int max=1;
int b=0;
StringTokenizer t=new StringTokenizer(s1," ");
while(t.hasMoreTokens()){ String s2=t.nextToken(); int n=0;
for(int i=0;i<s2.length()-1;i++) if(s2.charAt(i)==s2.charAt(i+1)) n++;
if(n>max)
{
max=n; b=max+1;
}
}
return b;
}
}
44.	Unique Characters in a string
Main
import java.util.*;
import java.text.*;


public class Main {
 
public static void main(String[] args) throws ParseException { Scanner sc = new Scanner(System.in);
String s1 = sc.nextLine(); System.out.println(UserMaincode.uniqueCounter(s1));
}}
UserMainCode  class UserMaincode
{
public static int uniqueCounter(String s1)
{

StringBuffer sb = new StringBuffer(s1); for (int i = 0; i < sb.length(); i++) { int count = 0;
for (int j = i + 1; j < sb.length(); j++) { if (sb.charAt(i) == sb.charAt(j)) { sb.deleteCharAt(j);
j--;
count++;
}
}
if (count >= 1) { sb.deleteCharAt(i); i--;
}
}
return sb.length();
}
}

45.	Name Shrinking
 
Main
import java.text.*;
import java.util.*;

public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in);
String s1=sc.nextLine(); System.out.println(UserMainCode.getFormatedString(s1));
}
}

UserMainCode
class UserMainCode
{


public static String getFormatedString(String s1) { StringBuffer sb=new StringBuffer();
StringTokenizer st=new StringTokenizer(s1," "); String s2=st.nextToken();
String s3=st.nextToken(); String s4=st.nextToken(); sb.append(s4).append(" "); sb.append(s3.substring(0,1)); sb.append("."); sb.append(s2.substring(0,1)); return sb.toString();
}
}
46.	Odd Digit Sum
 
Main
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner sc = new Scanner(System.in);
int s1=sc.nextInt();
String[] s2 = new String[s1]; for (int i = 0; i < s1; i++) { s2[i] = sc.next();
}
System.out.println(UserMainCode. oddDigitSum(s2));
}}

UserMainCode

public class UserMainCode {
public static int oddDigitSum (String[] s1) {
int sum=0;
for(int i=0;i<s1.length;i++) for(int j=0;j<s1[i].length();j++){ char c=s1[i].charAt(j); if(Character.isDigit(c)){ if(c%2!=0)
{
String t=String.valueOf(c); int n=Integer.parseInt(t); sum=sum+n; } }}
return sum;
}
}
47.	Unique Number 

import java.util.*;
import java.text.*;

public class Main{
public static void main(String[]args)
{int j=0;
Scanner sc=new Scanner(System.in); int n=sc.nextInt(); j=UserMainCode.getUnique(n); if(j>0)
{
System.out.println("Not Unique");
}
else if(j==0)
{
System.out.println("Unique");
}
}}


class UserMainCode
{
public static int getUnique(int n)
{
int []a=new int[100]; int i=0,count=0; while(n!=0)
{
int num=n%10; a[i]=num; i++;
n=n/10;
}
for(int j=0;j<=i-1;j++)
{
for(int k=j+1;k<=i-1;k++)
{
if(a[j]==a[k]){ count++;
}
}}
return count;
}

}

48.	Sum of Lowest marks
Main
import java.util.*;

public class Main {
public static void main(String args[]){ Scanner sc = new Scanner(System.in); int n=Integer.parseInt(sc.nextLine());
HashMap<Integer,Integer>h1=new HashMap<Integer,Integer>();
for(int i=0;i<n;i++)
{
h1.put(sc.nextInt(),sc.nextInt());
}
System.out.println(UserMainCode.getLowest(h1));
 
}
}
UserMainCode
class UserMainCode {
public static int getLowest(HashMap<Integer,Integer>h1)
{
ArrayList<Integer>a1=new ArrayList<Integer>();
int m=0;
Iterator<Integer> it=h1.keySet().iterator();
while(it.hasNext())
{
int x=it.next(); a1.add(h1.get(x));
}
Collections.sort(a1); m=a1.get(0)+a1.get(1)+a1.get(2); return m;
}}
49.	Color Code Validation same as 21
Main
import java.util.*;
public class Add {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.next();
boolean b=userMainCode. validateColourCode (s1);
if(b==true)
 
System.out.println("valid color code");
else
System.out.println("invalid color code");
}

UserMainCode

static class userMainCode{
public static boolean validateColourCode (String s1)

boolean b=false;
if(s1.length()==7&&s1.matches("#[A-F0-9]{1,}")){ b=true; 
}
}}}

return b;
 
50.	Repeating set of characters in a string
Main
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s= new Scanner(System.in); String input= s.next();
 
int n=s.nextInt(); System.out.println(userMainCode.getString(input,n));

}
}

UserMainCode
class userMainCode {

public static String getString(String input, int n){ StringBuffer sb=new StringBuffer();
sb.append(input);
for (int i=0;i<n;i++){
sb.append(input.substring(input.length()-n,input.length()));
}
return sb.toString();
}
}

51.	Finding the day of birth
Main
import java.util.*; import java.text.*; public class Main {

public static void main(String[] args) throws ParseException { Scanner s= new Scanner(System.in);
String input= s.next(); System.out.println(userMainCode.calculateBornDay(input)); 
}

}
UserMainCode
class userMainCode{
public static String calculateBornDay(String input) throws ParseException{ SimpleDateFormat sdf= new SimpleDateFormat("dd-MM-yyyy"); SimpleDateFormat sdf1= new SimpleDateFormat("EEEEE");
Date d= sdf.parse(input); String s1= sdf1.format(d); return s1;
}
}

52.	Removing elements from HashMap
Main
import java.util.*; import java.text.*; public class Main {

public static void main(String[] args) { Scanner s= new Scanner(System.in);
HashMap<Integer, String>hm=new HashMap<Integer, String>();
int n= s.nextInt();
for(int i=0;i<n;i++){
hm.put(s.nextInt(),s.next());
}

System.out.println(UserMainCode.afterDelete(hm)); s.close();
}

}

UserMainCode
class UserMainCode{
public static int afterDelete(HashMap<Integer, String> hm){ int count=0; Iterator<Integer>itr=hm.keySet().iterator(); while(itr.hasNext())
{
int n=itr.next();
if(n%3!=0)
{
count++;
}
}
return count;

}
}

53.	Experience Calculator
Main
import java.util.*; import java.text.*; public class Main {
public static void main(String[] args)throws ParseException { Scanner sc=new Scanner(System.in);
String a=sc.next();
String b=sc.next();
int c=sc.nextInt();
long res=(userMainCode.calculateExperience(a,b,c));
if(res==c)
{
System.out.println("true");
}
else
System.out.println("false");
}

}
UserMainCode
class userMainCode{
public static long calculateExperience(String a, String b, int c)throws ParseException{

SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); Date d=new Date();
Date d1=new Date(); d=sdf.parse(a); d1=sdf.parse(b);  long t=d.getTime(); long t1=d1.getTime(); long t3=t1-t;
long l1=(24 * 60 * 60 * 1000);
 
long l=l1*365; long res=t3/l; return res;
}
}
54.	Flush Characters
Main:
import java.util.*; import java.text.*; public class Main {
public static void main(String[] args) { Scanner s= new Scanner(System.in); String input=s.next();
System.out.println(UserMainCode.getSpecialChar(input));

}

}

UserMainCode:
class UserMainCode{
public static String getSpecialChar(String input){
int i;
StringBuffer sb= new StringBuffer();
for(i=0;i<input.length();i++)
{
char a=input.charAt(i);
if (!Character.isAlphabetic(a)) sb.append(a);
}
return sb.toString();
}
 
}

55.	String Repetition
class Main{
public static void main(String[] args) {
Scanner s= new Scanner(System.in); System.out.println(“enter a string”); String input= s.next();
int n= s.nextInt(); System.out.println(UserMainCode.repeatString(input, n));

}

}

class UserMainCode{
public static String repeatString(String input, int n){ StringBuffer sb= new StringBuffer();
String s1= new String();
if (n==1){
s1=input.substring(0,1); sb.append(s1).append(" ");
}
if(n==2){
s1=input.substring(0,2); for(int i=0;i<n;i++) sb.append(s1).append(" ");
}
if(n>=3){
 
s1=input.substring(0,3); for(int i=0;i<n;i++) sb.append(s1).append(" ");
}
return sb.toString();
}
}
56.	Average of Prime Locations

Main:
import java.util.*; import java.text.*; public class Main {

public static void main(String[] args) { Scanner s= new Scanner(System.in);
int n,i;
System.out.println("enter the array size"); n=s.nextInt();
int array[]=new int[n]; for(i=0;i<n;i++){
array[i]=s.nextInt();
 
}
System.out.println(UserMainCode.AverageElements(array)); s.close();
}

}

UserMainCode:
class UserMainCode{
public static double AverageElements(int array[]){
int n, sum=0,count=0,count1=0; double average; n=array.length;
for(int i=0;i<=n;i++){
for(int j=1;j<n;j++){
if(i%j==0)
count++;
if(count==2){
sum= sum+array[i]; count1++;
}
}
}
average= sum/count1;
DecimalFormat df=new DecimalFormat("#.00");
double ddd=Double.parseDouble(df.format(average));

return ddd;
}
}
57.	Common Elements
Main:
import java.util.*; public class Main { private static Scanner s ;
;
public static void main(String[] args) { s = new Scanner (System.in);
int n = s.nextInt(); int a[] = new int[n]; int b[] = new int[n]; for(int i=0;i<n;i++)
{
a[i] = s.nextInt();
}
for(int i=0;i<n;i++)
{
b[i] = s.nextInt();
}
System.out.println(UserMainCode.sumCommonElements(a, b));
}
}
UserMainCode:
public class UserMainCode {
public static int sumCommonElements(int a[],int b[]){ int sum = 0 ;
for(int i=0;i<a.length;i++)
{
for(int j=0;j<b.length;j++){ if(a[i]==b[j])
sum = sum + a[i];}
}
if(sum==0) return -1;
else return sum;
}
}
58.	Middle of Array
Main:
import java.util.*; public class Main { private static Scanner s;
public static void main(String[] args) {
s = new Scanner(System.in);
int n = s.nextInt(); int[] a = new int[n]; for(int i=0;i<n;i++){
a[i] = s.nextInt();
}
System.out.println(UserMainCode.getMiddleElement(a));
}
}
UserMainCode:
public class UserMainCode {
public static int getMiddleElement(int a[]){
int n = a.length;
return a[n/2];
}
 }
59.	Simple String Manipulation
Main:
import java.util.*;

public class Main {

private static Scanner s;

public static void main(String[] args) {

s = new Scanner(System.in); String s1 = s.next();
System.out.println(UserMainCode.getString(s1));
}
}
UserMainCode:
public class UserMainCode {
public static String getString(String s1){ StringBuffer sb=new StringBuffer(); char a=s1.charAt(0);
char b=s1.charAt(1); 
if(a!='j'&& b!='b') sb.append(s1.substring(2)); else if(a=='j' && b!='b')
sb.append("j").append(s1.substring(2)); else if(a!='j' && b=='b') sb.append(s1.substring(1));
else sb.append(s1.substring(0)); return sb.toString();
}
}
60.	Date Validation

Main:
import java.util.*;

public class Main {

public static void main(String[] args) { Scanner sc = new Scanner(System.in);
String s= sc.next();

int b = UserMainCode.getvalues(s);

if(b==1)

System.out.println("Valid");
 
else

System.out.println("Invalid");

}

}



UserMainCode:

import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.Date;
public class UserMainCode {

public static int getvalues(String s) {

if(s.matches("[0-9]{2}[.]{1}[0-9]{2}[.]{1}[0-9]{4}"))

{

SimpleDateFormat sdf=new SimpleDateFormat("dd.MM.yyyy");

sdf.setLenient(false);

try

{

Date d1=sdf.parse(s);

return 1;

} catch (ParseException e) {

return -1;

}

}

else if(s.matches("[0-9]{2}[/]{1}[0-9]{2}[/][0-9]{4}"))

{

SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy");

sdf.setLenient(false);

try

{

Date d1=sdf.parse(s);
 
return 1;

} catch (ParseException e) {

return -1;

}

}

else if(s.matches("[0-9]{2}[-]{1}[0-9]{2}[-][0-9]{4}"))

{

SimpleDateFormat sdf=new SimpleDateFormat("dd-MM-yyyy");

sdf.setLenient(false);

try

{

Date d1=sdf.parse(s);

return 1;

} catch (ParseException e) {

return -1;

}

}

else return -1;
}

}


61.	Boundary Average


Main:
import java.util.*;

import java.util.Arrays;

public class Main {

public static void main(String[] args) { Scanner sc = new Scanner(System.in);
int s = sc.nextInt();

int a[] = new int[s];

for (int i = 0; i < s; i++) a[i] = sc.nextInt();
System.out.println(UserMainCode.getBoundaryAverage(a));

}

}

UserMainCode

import java.util.Arrays;

public class UserMainCode {

public static float getBoundaryAverage(int a[] ){ Arrays.sort(a);
int sum = a[0] + a[a.length - 1];

float avg = (float) sum / 2;

return avg;

}

}
 
62.	Count Vowels

Main:
import java.util.*; public class Main { private static Scanner s;

public static void main(String[] args) { s = new Scanner(System.in);
String s1= s.next();
System.out.println(countVowels(s1));
}

UserMainCode
public class UserMainCode{
public static int countVowels(String s1)
{
String s2=s1.toLowerCase(); String s3="aeiou";
int count=0;
for(int i=0;i<s2.length();i++)
{
for(int j=0;j<s3.length();j++)
{
if(s2.charAt(i)==s3.charAt(j))
{
count++;
}
}
}
return count;
}
}

63.	Month Name

Main:
import java.text.ParseException; import java.util.Scanner;
public class Main {
public static void main(String[] args) throws ParseException {

Scanner sc=new Scanner(System.in); String s1=sc.nextLine();
System.out.println(UserMainCode.calculateBornDay(s1)); sc.close();
}
}

UserMainCode:
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.Date;
public class UserMainCode {
public static String calculateBornDay(String s1) throws ParseException
{
SimpleDateFormat sdf=new SimpleDateFormat("dd-MM-yy"); SimpleDateFormat sdf1=new SimpleDateFormat("MMMM"); Date d=sdf.parse(s1);
String s=sdf1.format(d); return s.toUpperCase();
}
}


64.	Reverse SubString

Main:
import java.util.*; public class Main { private static Scanner s;
public static void main(String[] args) { s =new Scanner(System.in);
String input1= s.next();
int input2=s.nextInt();int input3=s.nextInt(); System.out.println(UserMainCode.retrieveString(input1,input2,input3));
}
}

UserMainCode
class UserMainCode {
public static String retrieveString(String input1, int input2, int input3) { StringBuffer sb=new StringBuffer(input1);
sb.reverse();
String output=sb.substring(input2, input2+input3); return output;
}
}
65.	String Finder


USERMAINCODE:

public class UserMainCode {
public static int stringFinder(String s1,String s2,String s3)
{
String a1=s1.toLowerCase(); String a2=s2.toLowerCase(); String a3=s3.toLowerCase();
if(a1.contains(a2)&&a1.contains(a3))
{
if(a1.indexOf(a2)<a1.indexOf(a3))
{
 

}
else

}
 
return 1;


return 2;
 

}}

MAIN:
 
return 0;
 

import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.next();
String s2=s.next(); String s3=s.next();
int b=UserMainCode.stringFinder(s1, s2, s3);
if(b==1)
{
 

}
else
 
System.out.println("yes");


System.out.println("No");
 
s.close();
}

}

66.	Phone Number Validator

USERMAINCODE:

public class UserMainCode {

public static int validatePhoneNumber(String s1)

{

String s2 = s1.replaceAll("-", "");

if (s2.matches("[0-9]{10}"))

{

return 1;

}

else

return 2;

}

}
 
MAIN:

import java.util.*;

public class Main {

public static void main(String[] args) {

Scanner s=new Scanner(System.in); String s1=s.nextLine();
int b=UserMainCode.validatePhoneNumber(s1);

if(b==1)

{

System.out.println("Valid");

}

else

System.out.println("Invalid"); s.close();
}

}


67.	Month : Number of Days
USERMAINCODE:

import java.util.Calendar;
public class UserMainCode {
public static int getNumberOfDays(int y,int c)
{
 


}
}
MAIN:
 
Calendar cal=Calendar.getInstance(); cal.set(Calendar.YEAR, y); cal.set(Calendar.MONTH, c);
int day=cal.getActualMaximum(Calendar.DAY_OF_MONTH);
return day;
 

import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
int y=s.nextInt();
int c=s.nextInt(); System.out.println(UserMainCode.getNumberOfDays(y, c)); s.close();
}
}

68.	Negative String

USERMAINCODE:

public class UserMainCode {
public static String negativeString(String s1)
{
 

}
}

MAIN:
 
String str=s1.replace(" is ", " is not ");
return str;
 

import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.nextLine();
System.out.println(UserMainCode.negativeString(s1)); s.close();
}
}

69.	Validate Number


USERMAINCODE:

public class UserMainCode {
public static String validateNumber(String s1)
 
{	String ss="-1";
if (s1.matches("[-]{1}[0-9]{1,}"))
{
 

}
else
 
String st=s1.replace("-","");
return st;
 
}
MAIN:
 
return ss;
}

import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.next();
System.out.println(UserMainCode.validateNumber(s1)); s.close();
}
}

70.	Digits

USERMAINCODE:

public class UserMainCode {
public static int countSeven(int n)
{
int rem,sum=0;
 
while(n>0)
{
rem=n%10;
if(rem==7)
{
sum++;
}
n=n/10;
}
return sum;
}
}

MAIN:

import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); int n=s.nextInt();
System.out.println(UserMainCode.countSeven(n)); s.close();
}
}
71.	String Processing – III

USERMAINCODE:

public class UserMainCode {
public static String moveX(String s1)
{
 
String s2=""; String s3="";
for(int i=0;i<s1.length();i++)
{
char c=s1.charAt(i);
if(c=='x')
{
s2=s2+s1.charAt(i);
}
else
{
s3=s3+s1.charAt(i)
}

}

}

MAIN:
 
}
String st=s3.concat(s2);
return st;
 

import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.next();
System.out.println(UserMainCode.moveX(s1)); s.close();
} }

72.	String Processing – IV


USERMAINCODE:

public class UserMainCode {
public static String getStringUsingNthCharacter(String s1,int n)
{
StringBuffer sb=new StringBuffer(); sb.append(s1.charAt(0));
for(int i=n-1;i<s1.length();i+=n)
{
sb.append(s1.charAt(i));

} }


MAIN:
 
}
return sb.toString();
 

import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.next();
int n=s.nextInt(); System.out.println(UserMainCode.getStringUsingNthCharacter(s1, n)); s.close();
}


}
73.	Digit Comparison

UserMainCode
public class UserMainCode {
public static boolean compareLastDigit(int c,int d)
{

}
}
Main
 
int  c1=c%10; int d1=d%10; boolean b=false; if(c1==d1)
{
b=true;
}
return b;
 
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in);
int c=s.nextInt();
int d=s.nextInt();
boolean res=UserMainCode.compareLastDigit(c,d);
if(res==true)
{
System.out.println("TRUE");
}

else
{

}
 
System.out.println("FALSE");

s.close();
}

}

74.	Duplicates

UserMainCode:
public class UserMainCode {
public static int getDistinctSum(int a,int b,int c)
{
int sum;
if(a==b)
{
sum=c;
}
else if(b==c)
{
}
sum=a;
 else if(c==a)
{
 
}
else
{

}
 sum=b;
sum=a+b+c;
 return sum;
}

}

Main:

import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in); int a=s.nextInt();
 int b=s.nextInt();
int c=s.nextInt();
int sum=UserMainCode.getDistinctSum(a, b, c); System.out.println(sum);
s.close();

}

}

75.	String Processing - MixMania

UserMainCode

public class UserMainCode {
public static boolean checkPattern(String str)
{
String str1=str.substring(0,3);
int a=0,b=0,c=0;
char c1=str1.charAt(0); char c2=str1.charAt(1); char c3=str1.charAt(2); boolean b1=false;
if(Character.isDigit(c1)||Character.isLetter(c1))
{
a=1;
}
 
if(c2=='i')
{

}
 


b=1;
 
if(c3=='x')
{
c=1;
}

if(a==1&&b==1&&c==1)
{
b1=true;
 
}
return b1;
}

}

Main:
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in); String str=s.nextLine();
boolean b2=UserMainCode.checkPattern(str);
if(b2==true)
{
s.close();
}

}
else
{

}
 System.out.println("TRUE");
System.out.println("FALSE");
}
76.	String Processing
UserMainCode
public class UserMainCode {
public static String exchangeCharacters(String s1)
{
String s2=s1.substring(1,s1.length()-1); StringBuffer sb=new StringBuffer();
char c1=s1.charAt(0);
char c2=s1.charAt(s1.length()-1); sb.append(c2).append(s2).append(c1); return sb.toString();
}
 
}
Main:
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.next();

System.out.println(UserMainCode.exchangeCharacters(s1)); s.close();
}
}


77.	Regular Expression - II
UserMainCode:
public class UserMainCode {
public static boolean validateString(String s1)
{
boolean b=false;
if(s1.length()==3)
{
if(s1.matches("[a-zA-z]{3}"))
{
b=true;
 
}

}
return b;
}

}
Main:
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.next();
boolean b1=userMainCode.validateString(s1);
if(b1==true)
{
System.out.println("TRUE");
}
else
{
System.out.println("FALSE");
}

s.close();
}

}


78.	Strings Processing - Replication
UserMainCode:
public class UserMainCode {
public static String repeatString(String s1,int n)
{
StringBuffer sb=new StringBuffer();
for(int i=0;i<n;i++)
 
{
sb.append(s1);
}
return sb.toString();
}

}


Main:
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.next();
int n=s.nextInt(); System.out.println(UserMainCode.repeatString(s1, n));
s.close();
}

}


79.	SumOdd
UserMainCode:
public class UserMainCode {
public static int addOddNumbers(int n)
{
int sum=0;
for(int i=1;i<=n;i+=2)
{
sum=sum+i;
}
return sum;
}
 
}
Main:
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in);
int n=s.nextInt(); System.out.println(UserMainCode.addOddNumbers(n)); s.close();

}
}


80.	String Processing - V
UserMainCode:
public class UserMainCode {
public static String concatString(int n,String[] s1)
{
StringBuffer sb=new StringBuffer();
for(int i=0;i<s1.length;i++)
{
sb.append(s1[i]).append(",");
}
String s2=sb.toString();
String s3=s2.substring(0,s2.length()-1);

return s3;
}

}
 
Main:
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in);
int n=s.nextInt();
String s1[]=new String[n];
for(int i=0;i<n;i++)
{
s1[i]=s.next();
}
System.out.println(UserMainCode.concatString(n, s1)); s.close();
}

}
81.	Unique Number

Main:
import java.util.*;
public class Main {
public static void main(String[]args){ Scanner s=new Scanner(System.in); int a=s.nextInt();
int b=s.nextInt();
int c=s.nextInt(); System.out.println(UserMainCode.calculateUnique(a, b, c));
 
s.close();
}
}


UserMainCode:
public class UserMainCode {
public static int calculateUnique(int a,int b,int c)
{
int d=0;
if(a!=b&&a!=c&&b!=c)
{ d=3;
}
else if(a==b&&a==c&&b==c)
{ d=1;
}
else if((a!=b&&a==c&&b==c) || (a!=b&&a!=c&&b==c))
{ d=2;
}
else if((a==b&&a!=c&&b==c) || (a==b&&a!=c&&b!=c))
{ d=2;
}
else if((a==b&&a==c&&b!=c) || (a!=b&&a==c&&b!=c))
{
d=2;
}

return d;
}}



82.	Math Calculator
Main:
import java.util.*;
public class Main {
public static void main(String[]args){ Scanner s=new Scanner(System.in); int a=s.nextInt();
int b=s.nextInt();
char c = s.next().trim().charAt(0); System.out.println(UserMainCode.calculator(a, b, c)); s.close();
}}

UserMainCode:
public class UserMainCode {
public static int calculator(int a,int b,char c)
{
int a1=0;


if(c=='*')
{
a1=a*b;
}
else if(c=='+')
{
a1=a+b;
}
else if(c=='-')
{
a1=a-b;
}
else if(c=='/')
{
a1=a/b;
}
else if(c=='%')
{
a1=a%b;
}
return a1;
}}

83.	Scores

Main:
import java.util.*;
public class Main {
public static void main (String[] args)
{
Scanner sc = new Scanner(System.in);
int n = sc.nextInt(); int[] arr = new int[n]; for(int i=0;i<n;i++){ arr[i] = sc.nextInt();
}
System.out.println(UserMainCode.checkScores(arr, n)); sc.close();
}
}
UserMainCode:
public class UserMainCode {
public static boolean checkScores(int arr[], int n){
boolean b = false; for(int i=0;i<n-1;i++){ if(arr[i] == 100){
if(arr[i+1] == 100){ b = true;
break;
}
}
}
return b;
}
}

84.	ArrayFront
Main:
import java.util.*;

public class Main {

public static void main(String []args){ Scanner sc=new Scanner(System.in); int s=sc.nextInt();
int []a=new int[s]; for(int i=0;i<s;i++)
{

a[i]=sc.nextInt();

}
 
if(UserMainCode.scanArray(a)==true) System.out.println("TRUE");
else

System.out.println("FALSE"); sc.close();
}

}

UserMainCode:
public class UserMainCode {
public static boolean scanArray(int[] a)
{
int u=0,l=0; boolean b=false; if(a.length>=4) l=4;
else
l=a.length;
for(int i=0;i<l;i++)
if(a[i]==9) u=10;
if(u==10) b=true; return b;
}
}
85.	Word Count

Main:
import java.util.*;
public class Main {
public static void main(String []args){ Scanner sc=new Scanner(System.in); int n=sc.nextInt();
String[] str=new String[n];
for(int i=0;i<n;i++)
{
str[i]=sc.next();
}
int c=sc.nextInt(); System.out.println(UserMainCode.countWord(n,str,c)); sc.close();
}}

UserMainCode:
public class UserMainCode {
public static int countWord(int n,String str[],int c)
{
int count=0;
for(int i=0;i<str.length;i++)
{
if(str[i].length()==c)
{
count++;
}
}
return count;
}
}


86.	Find Distance

Main:
import java.util.*;
public class Main {
public static void main (String[] args)
{
Scanner s=new Scanner(System.in);
int a=s.nextInt(); int b=s.nextInt(); int c=s.nextInt(); int d=s.nextInt();
System.out.println(UserMainCode.findDistance(a,b,c,d)); s.close();
}
}
UserMainCode:
public class UserMainCode {
public static int findDistance(int a,int b,int c,int d) {
long q=(int)Math.round(Math.sqrt(((a-c)*(a-c))+((b-d)*(b-d))));
return (int) q;
}
}

87.	Word Count - II

Main:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
String s1=s.nextLine(); UserMainCode.countWord(s1); s.close();
}
}
UserMainCode:

import java.util.StringTokenizer;
public class UserMainCode {
public static void countWord(String s1){ StringTokenizer st=new StringTokenizer(s1," "); int n=st.countTokens();
System.out.println(n);
}
}


88.	Sum of Max & Min
 
Main:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); int a=s.nextInt();
int b=s.nextInt();
int c=s.nextInt(); System.out.println(UserMainCode.getSumMaxMin(a,b,c)); s.close();
}}

UserMainCode:
public class UserMainCode {
public static int getSumMaxMin(int a,int b,int c)
{
int d=0;
if(a<b&&b<c)
{
d=a+c;
}
else if(a<b&&b>c)
{
d=b+c;
}
else if(a>b&&b<c)
{
d=a+b;
}
return d;
}}

89.	Decimal to Binary Conversion

MAIN
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
int n=s.nextInt(); System.out.println(UserMainCode.convertDecimalToBinary(n));
 
s.close();
}
}

UserMainCode
public class UserMainCode {
public static long convertDecimalToBinary(int n){ String s1=Integer.toBinaryString(n);
long y=Long.parseLong(s1);
return y;
}
}

90.	String Processing - V
MAIN
import java.util.Scanner;
public class Main
{

public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String s1=s.nextLine();
int n1=s.nextInt(); System.out.println(UserMainCode.returnLastRepeatedCharacters(s1,n1)); s.close();
}
 
}
USERMAINCODE
public class UserMainCode{
public static String returnLastRepeatedCharacters(String s1, int n1)
{
StringBuffer sb = new StringBuffer();
for(int i = 0 ; i < n1 ; i++) sb.append(s1.substring(s1.length()-n1, s1.length())); return sb.toString();
}
}


91.	Regular Expression - III

MAIN
import java.util.Scanner;

public class Main {

public static void main(String[] args)

{

Scanner s=new Scanner(System.in); String s1=s.nextLine();
 
if(UserMainCode.validateString(s1)==true) System.out.println("TRUE");

else System.out.println("FALSE"); s.close();
}

}

USERMAINCODE
public class UserMainCode {
public static boolean validateString(String s)
{
boolean b=false;
if(s.charAt(0)=='0'||s.charAt(0)=='1'||s.charAt(0)=='2'||s.charAt(0)=='3'|| s.charAt(0)=='4'||s.charAt(0)=='5'||s.charAt(0)=='6'||s.charAt(0)=='7'||s.charAt(0
)=='8'||s.charAt(0)=='9'){


}
else

return b;
}
}
 
b=false; b=true;

92.	String Processing - TrimCat

MAIN
import java.util.Scanner;
public class Main
{
public static void main(String[] args)
 
{
Scanner s=new Scanner(System.in);
String s1=s.nextLine(); System.out.println(UserMainCode.getAlternateChars(s1)); s.close();
}
}
USERMAINCODE
public class UserMainCode{
public static String getAlternateChars(String s)
{
//String s1=s.replaceAll(“ “, “”); StringBuffer sbf = new StringBuffer(); for(int i = 0; i < s.length() ; i=i+2)
{
sbf.append(s.charAt(i));
}
String str = sbf.toString();
return str;
}
}


93.	String Processing - Username

MAIN CLASS
import java.util.Scanner;

public class Main {
public static void main(String[] args) { Scanner s=new  Scanner(System.in); String s1=s.nextLine();
System.out.println(UserMainCode.fetchUserName(s1));; s.close();
}
}
USERMAINCODE
 
import java.util.StringTokenizer;
public class UserMainCode {
public static String fetchUserName(String s1) { StringTokenizer st=new StringTokenizer(s1,"@"); String s2=st.nextToken();
return(s2);
}}


94.	String Processing - VII

import java.util.Scanner; public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.nextLine();
String s2=s.nextLine();

int n=s.nextInt();
 

boolean output=UserMainCode.isEqual(s1,s2,n);
System.out.println(output);	

s.close();

}

}

USERMAINCODE

public class UserMainCode {

public static boolean isEqual(String s1,String s2,int n){

boolean a=false;



if(n<s1.length()&&n<s2.length())

{

char c=s1.charAt(n);
char d=s2.charAt(s2.length()-n);

String s3=Character.toString(c);

//System.out.println(s3);

String s4=Character.toString(d);

//System.out.println(s4);

if(s3.equalsIgnoreCase(s4))

{

a=true;
 
}

else

{
a=false;
}
}

return a;
}
}

95.	Largest Difference
MAIN CLASS
 
import java.util.Scanner;
public class Main{
public static void main(String[] args) { Scanner s=new Scanner(System.in);
int m=s.nextInt();
int[] n1=new int[m]; for(int i=0;i<m;i++){
n1[i]=s.nextInt();
}
System.out.println(UserMainCode.checkDifference(n1)); s.close();
}
}
USERMAIN CODE
public class UserMainCode {
public static int checkDifference(int[] n1){
int n2,n3=0,n4=0,i; for(i=0;i<n1.length-1;i++){ n2=Math.abs(n1[i]-n1[i+1]); if(n2>n3){
n3=n2; n4=i+1; }}
return n4;
}
}

System.out.println(dsum);
}
}
}



96.	Start Case
MAIN CLASS
import java.util.Scanner;
 
public class Main {
public static void main(String[] args){ Scanner s=new Scanner(System.in); String s1=s.nextLine();
System.out.println(UserMainCode.printCapitalized(s1)); s.close();
}
}

USERMAIN CODE
import java.util.StringTokenizer;
public class UserMainCode{
public static String printCapitalized(String s1){ StringBuffer sb=new StringBuffer();
StringTokenizer t=new StringTokenizer(s1," ");
while(t.hasMoreTokens()){ String s2=t.nextToken(); String s3=s2.substring(0,1);
String s4=s2.substring(1, s2.length()); sb.append(s3.toUpperCase()).append(s4).append(" "); } return sb.toString();
}
}
97.	Maximum Difference
Main:
 
import java.util.Scanner;
public class Main {
public static void main(String[] args) {Scanner s=new Scanner(System.in);
int n=s.nextInt(); int a[]=new int[20]; for(int i=0;i<n;i++)
{
a[i]=s.nextInt();
}
s.close();
}

}
 
int max=UserMainCode.findMaxDistance(a); System.out.println(max);
 

UserMainCode:
public class UserMainCode {
static int findMaxDistance(int[] a)
{

int max=0,index=0;
for(int i=0;i<19;i++)
{
int d=Math.abs(a[i]-a[i+1]);
if(d>max)
{
max=d;
if(a[i]>a[i+1])
{
index=i;
}
else
{
index=i+1;
}
}
}
return index;

}
}


98.	Palindrome - In Range
Main:
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); int n1=s.nextInt();
int n2=s.nextInt(); System.out.println(UserMainCode.addPalindromes(n1,n2)); s.close();
}
}
UserMainCode:
public class UserMainCode {
public static int addPalindromes(int n1,int n2){
int sum=0;
for(int i=n1;i<=n2;i++){ int r=0,n3=i; while(n3!=0){ r=(r*10)+(n3%10);
n3=n3/10;
}
if(r==i) sum=sum+i;
}
return sum;
}
}


99.	PAN Card

Main:
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.nextLine();
UserMainCode.validatePAN(s1); s.close();
}
}


UserMainCode:
public class UserMainCode {public static void validatePAN(String s1) {
if(s1.matches("[A-Z]{3}[0-9]{4}[A-Z]{1}"))
{
System.out.println("Valid");
}
else
System.out.println("Invalid");
}
}


100.	Fibonacci Sum

Main:
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); int n=s.nextInt();
System.out.println(UserMainCode.getSumOfNfibos(n)); s.close();
}
}

UserMainCode:
public class UserMainCode {
public static int getSumOfNfibos(int n){ int a=-1,b=1,c=0,d=0;
for(int i=0;i<n;i++)
{
c=a+b; d=d+c; a=b; b=c;
}
return d;
}

}

101.	Test Vowels

Main:
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.nextLine();
int b=UserMainCode.testVowels(s1); if(b==1) System.out.println("Yes");
else
System.out.println("No"); s.close();
}
}

UserMainCode:
public class UserMainCode {

public static int testVowels(String s1) {
int b;
int n1=0,n2=0,n3=0,n4=0,n5=0;
String s2=s1.toLowerCase(); for(int i=0;i<s2.length();i++){ char  c=s2.charAt(i); if(c=='a')
n1++;
if(c=='e') n2++;
if(c=='i') n3++;
if(c=='o') n4++;
if(c=='u') n5++;}
if(n1==1&&n2==1&n3==1&&n4==1&&n5==1) b=1;
else b=2;
return b;
}

}

102.	Dash Check

import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in); String s1=s.nextLine();
String s2=s.nextLine();
int p=UserMainCode.compareDashes(s1,s2);
if(p==1) System.out.println("Yes"); else
System.out.println("No"); s.close();
}
}

import java.util.ArrayList;

public class UserMainCode {
public static int compareDashes(String s1, String s2) { ArrayList<Integer>l1=new ArrayList<Integer>();
for(int i=0;i<s1.length();i++)
{
if(s1.charAt(i)=='-')
{
l1.add(i);
}
}
ArrayList<Integer>l2=new ArrayList<Integer>();
for(int i=0;i<s2.length();i++)
{
if(s2.charAt(i)=='-')
{
l2.add(i);
}
}
//System.out.println(l1);
//System.out.println(l2);
if(l1.equals(l2))
 
{
return 1;
}
else
return 2;
}
}

8.	Reverse Split
import java.util.Scanner; public class Main {
public static void main(String[] args) {
Scanner s=new Scanner(System.in); String s1=s.nextLine();
String s2=s.next(); System.out.println(UserMainCode.reShape(s1,s2)); s.close();
}

}
public class UserMainCode {
public static String reShape(String s,String s1){ StringBuffer sb=new StringBuffer(s);
StringBuffer sb2=new StringBuffer(); String s2=sb.reverse().toString(); for(int i=0;i<s2.length();i++)
{
sb2.append(s2.charAt(i)); sb2.append(s1);
}
sb2.deleteCharAt(sb2.length()-1);
//System.out.println(sb2.toString()); return sb2.toString();
}


}

103.	Remove 10's
 

import java.io.*; import java.util.*; public class Main {
public static void main(String[] args) { Scanner sc = new Scanner(System.in); int i;
int n = sc.nextInt(); int a[] = new int[n]; for (i = 0; i < n; i++) {
a[i] = sc.nextInt();
}
UserMainCode.removeTens(a); sc.close();
}
 
}
import java.util.*;
public class UserMainCode {
public static void removeTens(int a[]){ Scanner sc = new Scanner(System.in);

int i,k = 0;
int b[] = new int[a.length];
ArrayList<Integer> al = new ArrayList<Integer>();
for (i = 0; i <a.length; i++) {
if (a[i] != 10) {
al.add(a[i]);
}
}
if (al.size() < a.length) { k = a.length- al.size(); for (i = 0; i < k; i++) { al.add(0);
}
}
int b1[] = new int[a.length]; for (i = 0; i < a.length; i++) { b1[i] = al.get(i); System.out.println(b1[i]);
}
}}

10.	Last Letters
public class Main {
 

public static void main(String[] args) { Scanner s=new Scanner(System.in); String input=s.nextLine();
System.out.println(UserMainCode.getLastLetter(input));

}

}
UserMainCode:
import java.util.*;
public class UserMainCode {
public static String getLastLetter(String input){ String str1=null;
StringTokenizer st=new StringTokenizer(input," "); StringBuffer sb=new StringBuffer(); while(st.hasMoreTokens()){
str1=st.nextToken();
/// String str2=Character.toString(str1.charAt(str1.length()-
 
1));
String str2=str1.substring(str1.length()-1); String str3= str2.toUpperCase(); sb.append(str3).append("$");
}sb.deleteCharAt(sb.length()-1);
return sb.toString();
}
}
 
104.	Largest Key in HashMap
Main:

import java.util.*;
public class Main {
/**
* @param args
*/
public static void main(String[] args) {
// TODO Auto-generated method stub
HashMap<Integer, String>hm=new HashMap<Integer, String>(); Scanner s=new Scanner(System.in);
int n=s.nextInt();
for(int i=0;i<n;i++)
{
int a=s.nextInt(); String s1=s.next(); hm.put(a,s1);

}
System.out.println(UserMainode.getMaxKeyValue(hm));

}
}


Hashmap:
import java.util.*;
import java.util.HashMap;
import java.util.Iterator;
public class UserMainode {
public static String getMaxKeyValue(HashMap<Integer, String> hm) {
int max=0; String s3=null;
Iterator<Integer>itr=hm.keySet().iterator();
while(itr.hasNext())
{
int b=itr.next();
if(b>max)
{
max=b; s3=hm.get(b);
}
}
return (s3);
}
}

All Numbers

Main:
import java.util.*; public class Main {
public static void main(String[] args) { Scanner s = new Scanner(System.in);
int n = s.nextInt();
String[] s1 = new String[n]; for(int i=0;i<n;i++){
s1[i] = s.next();
}
int out=(userMainCode.validateNumber(s1)); System.out.println(out);
}
}

UserMainCode:
class userMainCode{
public static int validateNumber(String[] s1)
{ 
int b=0,count,out=0;
for(int i=0;i<s1.length;i++){ String s2 = s1[i]; 
if(s2.matches("[0-9.]{1,}")) 
{	
count =0;
for(int j=0;j<s2.length();j++)

{
char c = s2.charAt(j); if(c=='.')
count++;
}

if(count>1)
b=1;
}
else b=1;
}
if(b==0)
{ 
out=1;
}
Else
 out=-1; 
return out;
}
}

Day of the Week
Main:
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.Date;
import java.util.Scanner;
public class Main {

public static void main(String[] args)throws ParseException { Scanner sc=new Scanner(System.in);
String s1=sc.nextLine(); System.out.println(UserMainCode.getDay(s1));
}
// TODO Auto-generated method stub

}
UserMainCode:
import java.text.SimpleDateFormat; import java.text.ParseException; import java.util.Date;
public class UserMainCode {

public static String getDay(String s1) throws ParseException
{
SimpleDateFormat sdf=new SimpleDateFormat("MM-dd-yyyy"); SimpleDateFormat sdf1=new SimpleDateFormat("EEEEE"); Date d=sdf.parse(s1);
String s=sdf1.format(d);
return s;
}
}


Max Substring
Main:
import java.util.*;
 
public class Main {
public static void main(String[] args){
Scanner sc=new Scanner(System.in); String input1=sc.next();
String input2=sc.next(); System.out.println(UserMainCode.extractMax(input1,input2));
}
}

Usermaincode:

import java.util.StringTokenizer;
import java.util.*;

public class UserMainCode {
public static String extractMax(String input1,String input2){
int max=0; String s3=null;
StringTokenizer st=new StringTokenizer(input1,"-");
while( st.hasMoreTokens())
{
String s2=st.nextToken(); int n=s2.length(); if(n>max)
{
max=n; s3=s2;
}
}
return(s3);
}}


States and Capitals
Main:
import java.util.HashMap; import java.util.Scanner; public class Main {

public static void main(String[] args) { Scanner sc=new Scanner(System.in); int n=sc.nextInt(); HashMap<String,String> hm=new HashMap<String,String>();
for(int i=0;i<n;i++)
{
String s1=sc.next(); String s2=sc.next(); hm.put(s1,s2);
}
String sa=sc.next(); System.out.print(UserMainCode.getCapital(hm,sa));
}


}


UserMainCode:
import java.util.HashMap; import java.util.Iterator; import java.util.Map; public class UserMainCode {
public static String getCapital(HashMap<String,String> hm,String sa)
{
String chan=null; Iterator<String>it=hm.keySet().iterator(); StringBuffer sb=new StringBuffer(); while(it.hasNext()){
String a=it.next();
if(a.equals(sa))
{
chan=hm.get(a);
 
sb.append(chan).append("$").append(sa);
}
}
return sb.toString();
}
}

	Simple String Manipulation - II

Main:
import java.util.*;
public class Main {

public static void main(String[] args) { Scanner sc=new Scanner(System.in); String inpList=sc.nextLine();
System.out.println(UserMainCode.calculateWordSum(inpList));
}

}
UserMainCode:
import java.util.*;
 
public class UserMainCode {
public static int calculateWordSum(String inp) {

int count=0;
String st[]=inp.split(" "); String s1=st[0];
String slst=st[st.length-1];
if(s1.equals(slst))
{
count=s1.length();
}
else
{
count=s1.length()+slst.length();
}
return count;
}
}

Vowels, Arrays & ArrayLists

Main:
package vowels;
import java.util.*;

public class Main {

public static void main(String[] args) {

int n;
Scanner sc=new Scanner(System.in); n=Integer.parseInt(sc.nextLine()); String[] str=new String[n]; for(int i=0;i<n;i++)
{
str[i]=sc.nextLine();
}
ArrayList<String> arr=new ArrayList<String>(); arr=UserMainCode.matchCharacter(str); Iterator<String> it=arr.iterator(); while(it.hasNext())
{
System.out.println(it.next());
}

}
}


Usermaincode:
package vowels;
import java.util.*;
public class UserMainCode {

public static ArrayList<String> matchCharacter (String[] ss)
{
ArrayList<String> as=new ArrayList<String>();
for(int i=0;i<ss.length;i++)
{
String sp=ss[i];
char[] mp=sp.toLowerCase().toCharArray();
if((mp[0]=='a'||mp[0]=='e'||mp[0]=='i'||mp[0]=='o'||mp[0]=='u')& &(mp[sp.length()-
1]=='a'||mp[sp.length()-1]=='e'||mp[sp.length()- 1]=='i'||mp[sp.length()-
1]=='o'||mp[sp.length()-1]=='u'))
{
as.add(sp);
}
}
return as;
}
}
 
	Transfer from Hashmap to Arraylist
main:
import java.util.*; import java.text.*; public class Main {
public static void main(String[] args) {
HashMap<Integer,String> hm1=new HashMap<Integer,String>();
int n;
Scanner sc=new Scanner(System.in); n=Integer.parseInt(sc.nextLine()); for(int i=0;i<n;i++)
{
hm1.put(Integer.parseInt(sc.nextLine()),sc.nextLine());
}
ArrayList<String> al1=new ArrayList<String>(); al1=UserMainCode.getName(hm1); Iterator<String> it=al1.iterator(); while(it.hasNext())
{
 
System.out.println(it.next());
}

}
}


Usermaincode:


import java.util.*;
import java.text.*;
public class UserMainCode {
public static ArrayList<String> getName(HashMap<Integer,String> hm1)
{
ArrayList<String> al2=new ArrayList<String>(); Iterator<Integer> it =hm1.keySet().iterator(); while(it.hasNext())
{
int id=it.next();
String name=hm1.get(id);
if(name.matches("[a-z]{1,}.*[0-9]{1,}.*[A-Z]{1}")) al2.add(name);
}
return al2;
}
}

	Max Admissions

import java.util.ArrayList; public class UserMainCode
{

public static int year (ArrayList<Integer> a1)

{

int max=0,pos=0;

for(int i=1;i<a1.size();i+=2)

{

if(a1.get(i)>max)

{

max=a1.get(i); pos=i;
}

}

return a1.get(pos-1);

}

} MAIN:
import java.util.*; class Main
{

public static void main(String [] args)

{

Scanner s=new Scanner(System.in); ArrayList<Integer> a1=new ArrayList<Integer>();
 
int n=s.nextInt(); n=n*2;
for(int i=0;i<n;i++)

{

a1.add(s.nextInt());

}

System.out.println(UserMainCode.year(a1)); s.close();
}

}



	Sum Non Prime Numbers

Main:
import java.util.*;
public class Main {
public static void main(String[] args) {
{
Scanner s=new Scanner(System.in);
int n=s.nextInt(); System.out.println(UserMainCode.addNumbers(n));
}
 
}
}
Usermaincode:

public class UserMainCode {
public static int addNumbers(int n) { int sum=0;int k=0;int sum1=0; for(int i=1; i<=n; i++)
{ k=0;
for(int j=1; j<=i; j++)
{
if(i%j==0) k++;
}
if(k!=2)
{
sum=sum+i;
}
}
return sum;
}
}

	Date Format Conversion
Main:
import java.util.*; import java.text.*; public class Main {
public static void main(String[] args) {
Scanner s=new Scanner(System.in); String s1=s.next(); UserMainCode.convertDateFormate(s1);
}
}

Usermaincode:
 
import java.util.*; import java.text.*;
public class UserMainCode {
public static void convertDateFormate(String s1) { SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); sdf.setLenient(false);
try {
Date d1=sdf.parse(s1);
SimpleDateFormat sdf1=new SimpleDateFormat("dd-MM-yy"); String s2=sdf1.format(d1);
System.out.println(s2);
} catch (ParseException e) { e.printStackTrace();
}
}
}

	Valid Date

public class UserMainCode
{
public static int dateformat(String s1) throws ParseException
{
String s2=" ";
 
    int n = -1;
if(s1.matches("[0-9]{2}[.]{1}[0-9]{2}[.]{1}[0-9]{4}"))
{
SimpleDateFormat sdf=new SimpleDateFormat("dd.MM.yyyy");
Date d=sdf.parse(s1);
s2=sdf.format(d);
n=1;
}
else if(s1.matches("[0-9]{2}[/]{1}[0-9]{2}[/]{1}[0-9]{2}"))
{
SimpleDateFormat sdf1=new SimpleDateFormat("dd/MM/yy");
Date d1=sdf1.parse(s1);
s2=sdf1.format(d1);
n=1;
}
else if(s1.matches("[0-9]{2}[-]{1}[0-9]{2}[-]{1}[0-9]{4}"))
{
SimpleDateFormat sdf2=new SimpleDateFormat("dd-MM-yyyy");
Date d2=sdf2.parse(s1);
s2=sdf2.format(d2);
n=1;
}
else
{
n=-1;
}

return n;
 
}

} MAIN:
import java.text.ParseException; import java.util.*;
class Main

{

public static void main(String [] args) throws ParseException

{

Scanner s=new Scanner(System.in); String s1=s.next();
int b=UserMainCode.dateformat(s1); if(b==1)
{

System.out.println("Valid");

}

Else

{

System.out.println("Invalid");

}
s.close();
}
}
23.	Convert Format

Main:
import java.util.*; import java.text.*; public class Main {
public static void main(String[] args) {
Scanner sc=new Scanner(System.in); String s=sc.next();
System.out.println(UserMainCode.convertFormate(s));
}

}

Usermaincode:
import java.util.*; import java.text.*;
public class UserMainCode {
public static String convertFormate(String s) { StringTokenizer t=new StringTokenizer(s,"-"); String s1=t.nextToken();
String s2=t.nextToken(); String s3=t.nextToken();
StringBuffer sb=new StringBuffer(); sb.append(s1.substring(0, s1.length()-1)).append('-');
sb.append(s1.charAt(s1.length()-1)).append(s2.charAt(0)).append('-');
sb.append(s2.substring(1, s2.length())).append(s3.charAt(0)).append('-'); sb.append(s3.substring(1, s3.length()));
return sb.toString();
}
}

	Add and Reverse
Main:
import java.util.*;


public class Main {

public static void main(String[] args)
{
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int a[]=new int[n];
for(int i=0;i<n;i++)
{
a[i]=sc.nextInt();
}
int b=sc.nextInt(); System.out.println(UserMainCode.addAndReverse(n,b,a)) ; sc.close();
}
}
Usermaincode:
import java.util.*;
public class UserMainCode {
 
public static int addAndReverse(int n,int b,int a[])
{


int i=0,sum=0,r=0;
for(i=0;i<a.length;i++)
{
if(a[i]>b)
{
sum=sum+a[i];
}
}
System.out.println(sum);
while(sum!=0)
{ r=((r*10)+(sum%10)); sum=sum/10;
}
return r;
}
}

	Next Year day

Main:
import java.util.*; import java.text.*; public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in);
String s1=sc.next();
UserMainCode u=new UserMainCode();
{
System.out.println(u.nextYearDay(s1));
}
}
}
Usercodemain: import java.util.*; import java.text.*;
 
public class UserMainCode
{
public String nextYearDay(String s1)
{
String s=null;
SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); sdf.setLenient(false);
try {
Date d1=sdf.parse(s1);
Calendar cal=Calendar.getInstance(); cal.setTime(d1); cal.add(Calendar.YEAR, 1);
Date d2=cal.getTime();
SimpleDateFormat sdf1=new SimpleDateFormat("EEEEE"); s=sdf1.format(d2);
}
catch (ParseException e)
{
e.printStackTrace();
}
return s;
}
}

	Sum Squares of Digits
Main:-
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
int n=s.nextInt(); UserMainCode.getSumOfSquaresOfDigits(n); s.close();

}
}


UserMainCode:-
import java.util.*;
 
public class UserMainCode {
public static void getSumOfSquaresOfDigits(int n) {
int a=n; int rem=0; int sum=0; while(a!=0)
{
rem=a%10; sum=sum+(rem*rem); a=a/10;
}
System.out.println(sum);
}
}

	Even and Odd Index Sum
Main:-
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner sc = new Scanner(System.in);
int n = sc.nextInt(); UserMainCode.sumOfOddEvenPositioned(n); sc.close();
}
 
}
UserMainCode:- import java.util.*;
public class UserMainCode {
public static void sumOfOddEvenPositioned(int n) {
int rem = 0, i = 0; int a[] = new int[10]; while (n > 0) {
rem = n % 10; a[i] = rem;
n = n / 10; i++;
}
int sume = 0, sumo = 0;
for (int j = i - 1; j >= 0; j--) {
if(j%2!=0)
{
sumo = sumo + a[j];
}
else
{
sume = sume + a[j];
}
}
if (sume == sumo) { System.out.println("Yes");
} else
System.out.println("No");
}
}



	Remove 3 Multiples
Main:-

import java.util.ArrayList; import java.util.Iterator; import java.util.Scanner; public class Main{
public static void main(String []args){  Scanner sc=new Scanner(System.in); ArrayList<Integer> al=new ArrayList<Integer>();
ArrayList<Integer> al1=new ArrayList<Integer>();
int n=Integer.parseInt(sc.nextLine());
for(int i=0;i<n;i++)
{
al.add(sc.nextInt());
}
al1=UserMainCode.removeMultiplesOfThree(al); Iterator it=al1.iterator(); while(it.hasNext())
{
System.out.println(it.next());
}
}
}

UserMainCode:-

import java.util.ArrayList; import  java.util.Iterator; import java.util.StringTokenizer; public class UserMainCode
{
public static ArrayList<Integer> removeMultiplesOfThree(ArrayList<Integer> al)
{
ArrayList<Integer> al2=new ArrayList<Integer>();
for(int i=0;i<al.size();i++)
{
if((i+1)%3!=0)
al2.add(al.get(i));
}
return al2;
}
}

	String Occurances - II
MAIN

import java.util.Scanner;
 
public class Main {

public static void main(String[]args){ Scanner sc=new Scanner(System.in); String s=sc.nextLine();
String s1=sc.nextLine(); System.out.println(UserMainCode.getSubstring(s, s1)); sc.close();
}

}

USERMAINCODE

public class UserMainCode{

public static int getSubstring(String s,String s1){ int t=s1.length();


int count=0;

for(int i=0;i<s.length()-t+1;i++)

{

String s3=s.substring(i,t+i); if(s3.equals(s1))
{

count++;
}
}

return count;

}
}
 
	Programming Logic

Main:-
import java.util.Scanner; public class Main{
public static void main(String[] args){ Scanner s=new Scanner(System.in);
int a=s.nextInt();

int b=s.nextInt(); int c=s.nextInt();
System.out.println(UserMainCode.luckySum(a,b,c));
}
}

UserMainCode:-
public class UserMainCode{
public static int luckySum(int a, int b, int c)
{
if(a == 13)
return 0;
if(b == 13) return a; if(c == 13)
return (a + b); return (a + b + c);
}
}

	Triplets
Main:-

import java.util.Scanner;

public class Main {

public static void main(String[] args)

{

int n;

Scanner sc=new Scanner(System.in);

n=sc.nextInt(); int[] a=new int[n]; for(int i=0;i<n;i++)
{

a[i]=sc.nextInt();

}

boolean s=UserMainCode.checkTripplets(a);

if(s==true) System.out.println("TRUE"); else System.out.println("FALSE");
}

}

UserMainCode:-

import java.util.*;

public class UserMainCode {

public static boolean checkTripplets(int[] a)

{
 
boolean b=false;


for(int i=0;i<a.length-2;i++)

{

if((a[i]==a[i+1])&&(a[i+1]==a[i+2]))

{

b=true;

}

}

return b;

}

}

	Repeat Front
Main:-

import java.util.*;

public class Main {

public static void main(String []args){ Scanner sc=new Scanner(System.in); String s=sc.nextLine();
int n=Integer.parseInt(sc.nextLine()); System.out.println(UserMainCode.repeatFirstThreeCharacters(s,n)); sc.close();
}
}

UserMaincode:-

import java.util.*;

public class UserMainCode

{

public static String repeatFirstThreeCharacters(String s,int n)

{
 
StringBuffer sb=new StringBuffer(); StringBuffer sb1=new StringBuffer(); if(s.length()>3)
{ sb.append(s.substring(0,3)); s=sb.toString();
}

for(int i=0;i<n;i++) sb1.append(s);
return sb1.toString();

}

}

Sorted Array

Main:-

import java.util.*;

public class Main

{

public static void main(String[] args)

{

int n;

Scanner sin = new Scanner(System.in);

n = sin.nextInt();

String[] a1 = new String[n];

for(int i=0;i<n;i++)

{

a1[i] = sin.next();

}

a1 = UserMainCode.orderElements(a1); for(int i=0;i<a1.length;i++) System.out.println(""+a1[i]);
}
}
UserMainCode:-
import java.util.*; 
public class UserMainCode
{
public static String[] orderElements(String[] arr)

{

HashSet<String> al=new HashSet<String>();
for(int i=0;i<arr.length;i++)
{
al.add(arr[i]);
}

Iterator<String> itr=al.iterator();

String ar[] = new String[al.size()];

int i =0 ;

while(itr.hasNext()){

ar[i] = itr.next(); i++;
}

Arrays.sort(ar);

return ar;

}

}



	Pattern Matcher
Main:
import java.util.*;

public class Main
{
public static void main(String[] args)

{
Scanner sc = new Scanner(System.in); String s = sc.next(); System.out.println(UserMainCode.CheckID(s)); sc.close();
}}

UserMainCode:

public class UserMainCode

{

public static boolean CheckID(String s)
 {
boolean b=false;
if(s.matches("(CPT)[-]{1}[0-9]{6}"))
{
b=true;
}
else
{
b=false;
}
return b;
}
}


	Playing with String - I

Main:

import java.util.Scanner;

public class Main
{
public static void main(String[] arg)
{
Scanner s=new  Scanner(System.in); int n=Integer.parseInt(s.nextLine()); String[] sc=new String[n];
for(int i=0;i<n;i++)
{
sc[i]=s.nextLine();
}

int a=Integer.parseInt(s.nextLine()); System.out.println(UserMainCode.formString(n,sc,a)); s.close();
}
}
 
UserMainCode:

public class UserMainCode {

public static String formString(int n,String[] input,int a)

{

StringBuffer sb=new StringBuffer();

for(int i=0;i<n;i++)

{

if(input[i].length()>=a)

{

String a1=input[i]; sb.append(a1.charAt(a-1));
}

else

{

sb.append('$');

}

}

return sb.toString();

}}

Regular Expression - 1
import java.util.Scanner;

public class Main {

public static void main(String []args){ Scanner sc=new Scanner(System.in); String n=sc.nextLine();
System.out.println(UserMainCode.validate(n)); sc.close();
}

}
 
public class UserMainCode

{

public static String validate(String s)

{

String w="FALSE";
if(s.length()==4 && (Character.isDigit(s.charAt(0))||Character.isAlphabetic(s.charAt(0)))&&s.charAt(1)
=='R')

{

if(Character.isDigit(s.charAt(2))) w="TRUE";
}

return w;

}

}

Regular Expression – 2 (Age Validator)


Main:

import java.util.*;

public class Main {

public static void main(String[]args){

Scanner s=new Scanner(System.in);	//Regular Expression – 2 (Age Validator) pg.No:150

String n=s.nextLine();

boolean b=UserMainCode.ValidateAge(n);

if(b==true)

{

System.out.println("TRUE");

}

else

System.out.println("FALSE");
 
s.close();

}

}

UserMainCode:

public class UserMainCode {

public static boolean ValidateAge(String n)

{

boolean b = false; if(n.matches("[0-9]{2}"))
{	//Regular Expression – 2
(Age Validator) pg.No:150

int a=Integer.parseInt(n);

if(a>0&&a>=21&&a<=45)

{

b=true;

}

else

b=false;



}

return b;



}}



Regular Expression – 3 (Phone Validator)

Main:

import java.util.*; public class Main {
public static void main(String[]args){ Scanner s=new Scanner(System.in); String s1=s.nextLine();
boolean b1=UserMainCode.validatePhone(s1); if(b1==true)
{	//phone validation pg.no:151
System.out.println("TRUE");
}
else
{
System.out.println("FALSE");
}
s.close();
}
}
 
UserMainCode:

public class UserMainCode {
public static boolean validatePhone(String s1)
{
boolean b=false; if(s1.matches("[0]{1}[0]{1}[0-9]{8}") )
{
b=false;
}
//phone validation pg.no:151
else
{
b=true;
}
return b;
}


}

String Splitter

import java.util.*;

public class Main

{

public static void main(String[] args)

{

Scanner s = new Scanner(System.in); String ip1=s.next();
char ip2='/';

String op[]=UserMainCode.manipulateLiteral(ip1,ip2); for(int i=0;i<op.length;i++) System.out.println(op[i]);
s.close();

}}

import java.util.ArrayList; import java.util.StringTokenizer; public class UserMainCode
{

public static String[] manipulateLiteral(String ip1, char ip2)

{

StringTokenizer t1 = new StringTokenizer(ip1,"/");

ArrayList<String> lst = new ArrayList<String>();

while(t1.hasMoreTokens())

{

StringBuffer sb = new StringBuffer(); sb.append(t1.nextToken().toLowerCase());
 
lst.add(sb.reverse().toString());

}

String[] op = new String[lst.size()];

for(int i = 0;i<lst.size();i++)

{

op[i] = lst.get(i);

}

return op;

}

}

Vowel Count

import java.util.*;

public class Main

{

public static void main(String[]args)	// Second set: 40.Vowel Count//

{

Scanner sc=new Scanner(System.in); String s=sc.nextLine();
int max=UserMainCode.tellVowelCount(s); System.out.println(max);
sc.close();

}

}

public class UserMainCode {

public static int tellVowelCount(String s)

{

int max=0;

int count=0;

for(int i=0;i<s.length();i++)

{

char c=s.charAt(i); if(c=='a'||c=='e'||c=='i'||c=='o'||c=='u'||c=='A'||c=='E'||c=='I'|| c=='O'||c=='U')
{

count++;

}

}

if(count>max)
 
{

max=count;

}

return max;

}

}
	Playing with String - II

import java.util.*;

public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in); int n=s.nextInt();
String s1[]=new String[n]; String s2[]=new String[n];
for(int i=0;i<n;i++)	//S.41.Playing with
String - II//

{
s1[i]=s.next();
}
s2=UserMainCode.sortArray(s1,n);
for (int i = 0; i < n; i++) { System.out.println(s2[i]);
}
s.close();
}}

import java.util.Arrays;

public class UserMainCode

{

public static String[] sortArray(String s1[],int n){
 
String s2[]=new String[n];

for (int i = 0; i < n; i++)

{

s2[i]=s1[i].toLowerCase();

}

Arrays.sort(s2);

return s2;

}
}

	Median Calculation

Main
import java.util.*;
public class Main
{
public static void main(String[] args)
{
 int n;
Scanner sin = new Scanner(System.in); n = sin.nextInt();
int[] a1 = new int[n]; for(int i=0;i<n;i++)
{

a1[i] = sin.nextInt();

}

System.out.println(""+UserMainCode.calculateMedian(a1)); sin.close();
}

}

UserMainCode
import java.util.Arrays;

public class UserMainCode

{

public static int calculateMedian(int[] a)

{

Arrays.sort(a);

int length = a.length;

int result=0,mid=0,midNext=0;

if((length%2) != 0)

{

mid = (length/2)+1;

result = a[mid];

}

else

{

mid = length/2;
 
midNext = mid+1;

float add = a[mid-1]+a[midNext-1];

float div = add/2;

result = Math.round(div);

}
return result;
}
}

	Sequence in Array
Main
import java.util.*;

public class Main
{
public static void main(String[] args)
{
Scanner s=new Scanner(System.in);
int n=s.nextInt();
int a[]=new int[n]; 
for(int i=0;i<n;i++){
a[i]=s.nextInt();
}
System.out.println(UserMainCode.searchsequence(a)); s.close();
}
}

UserMainCode
public class UserMainCode {

public static boolean searchsequence(int[] a)

{
boolean b = false;
for(int i = 0 ; i< a.length-3; i++)
{
if(a[i]==1 && a[i+1]==2 && a[i+2]==3) b = true;
}
return b;
}
}

	Asterisk & Characters
Main:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
String input=s.next();
System.out.println( UserMainCode. scanStarNeighbors (input)); s.close();
}
}

UserMainCode

import java.util.StringTokenizer;
 public class UserMainCode {
public static boolean scanStarNeighbors (String input) {
boolean b=false;
StringTokenizer t=new StringTokenizer(input,"*"); String s1=t.nextToken();
String s2=t.nextToken();
String s3=s1.substring(s1.length()-1); String s4=s2.substring(0,1); if(s3.equalsIgnoreCase(s4))
b=true;
return b;
}
}
	Occurance Count


Main
import java.util.*;

public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in);
String s1=s.nextLine();

String s2=s.nextLine();

int v=UserMainCode.countWords(s1,s2); System.out.println(v);
s.close();

}

}

UserMainCode
import java.util.StringTokenizer;

public class UserMainCode {

public static int countWords(String s1,String s2){ StringTokenizer t=new StringTokenizer(s1," "); int c=0;
 
while(t.hasMoreTokens())

{

String s3=t.nextToken();

if(s3.equals(s2)) c++;
}

return c;

}

}
	Regular Expressions - III

Main


import java.util.Scanner;

public class Main {

public static void main(String[] args) { Scanner s=new Scanner(System.in);
String s1=s.next(); String s2=s.next();
int v=UserMainCode.searchString(s1,s2); System.out.println(v);
s.close();

}

}

UserMainCode
public class UserMainCode {

public static int searchString(String s1,String s2){

int c=0;

int t=s2.length();

for(int i=0;i<s1.length()-t+1;i++){

if(s2.equals(s1.substring(i,t+i))){ c++;
}

}
 
return c;

}



}
	Strings Processing

Main

import java.util.Scanner;

public class Main

{

public static void main(String args[])

{

String str=new String();

Scanner sc=new Scanner(System.in); str=sc.nextLine();
int n=sc.nextInt();

String k=UserMainCode.findFruitName(str, n); System.out.println(k);
sc.close();

}

}

UserMainCode

import java.util.StringTokenizer;

public class UserMainCode

{

public static String findFruitName(String m,int n)

{

int i=0; String h=null;
StringTokenizer st=new StringTokenizer(m,",");

int max=st.countTokens(); String[] ss=new String[max]; while(st.hasMoreElements())
{

ss[i++]=st.nextToken();
 
}

if(n>max) h=ss[i-1]; else h=ss[n-1]; return h;
}

}

	Proper Case

Main

import java.util.*;

public class Main {

public static void main(String[] args){ Scanner s=new Scanner(System.in);
String s1=s.nextLine();
 
System.out.println(UserMainCode.changeCase(s1)); s.close();
}



}

UserMainCode
import java.util.StringTokenizer;

public class UserMainCode {

public static String changeCase(String s1){ StringBuffer s5=new StringBuffer(); StringTokenizer t=new StringTokenizer(s1," "); while(t.hasMoreTokens()){
String s2=t.nextToken(); String s3=s2.substring(0,1);
String s4=s2.substring(1, s2.length()); s5.append(s3.toUpperCase()).append(s4).append(" ");
}

return s5.toString();

}

}

	Length of same word


Main

import java.util.*;

public class Main {

public static void main(String[] args) { Scanner sc=new Scanner(System.in);


// TODO Auto-generated method stub String s1=sc.nextLine();
System.Out.Println(UserMainCode.compareLastWords(s1)); sc.close();
}

}

UserMainCode

import java.util.ArrayList;
 
import java.util.List;

import java.util.StringTokenizer;

public class UserMainCode {

public static int compareLastWords(String s1){ List<String> l=new ArrayList<String>(); StringTokenizer t=new StringTokenizer(s1," "); while(t.hasMoreTokens())
{

String s2=t.nextToken(); l.add(s2);
}

String s3=l.get(0);

String s4=l.get(l.size()-1);

if(s3.equals(s4))

{

int n=s3.length(); System.out.println(n);
}

else

{

int n1=s3.length(); int n2=s4.length(); int n=n1+n2;
}

Return n;

}

}

	Perfect Number

import java.util.*; public class Main {
public static void main(String[] args){ Scanner s=new Scanner(System.in); int n=s.nextInt();
boolean j=(UserMainCode.getPerfection(n)); if(j==true)
 
System.out.println("TRUE"); else System.out.println("FALSE");
}

}

public class UserMainCode {

public static boolean getPerfection(int n){ boolean b=false;
int sum=0;

for(int i=1;i<n;i++){ int r=n%i;
if(r==0) sum=sum+i;
}

b=(sum==n); return b;
}

}


	Find Digits



import java.util.*; public class Main {
public static void main(String[] args) {


Scanner s=new Scanner(System.in); double d=s.nextDouble();
System.out.println(UserMainCode.findNoDigits(d));

}}
 

import java.util.StringTokenizer;

public class UserMainCode {

public static String findNoDigits(double d) { int n1=0,n2=0;
String s=String.valueOf(d);

StringTokenizer t=new StringTokenizer(s,"."); String s1=t.nextToken();
String s2=t.nextToken(); n1=s1.length(); n2=s2.length(); if(s1.charAt(0)=='0') n1=s1.length()-1; if(n2!=1)
if(s2.charAt(s2.length()-1)=='0') n2=s2.length()-1;
String s3=String.valueOf(n1)+":"+String.valueOf(n2); return s3;
}

}


	Employees & Designations



import java.util.Iterator;
import java.util.LinkedHashMap; import java.util.Scanner;
public class Main {
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in); int k1=Integer.parseInt(sc.nextLine());
LinkedHashMap<String,String> hm=new LinkedHashMap<String,String>(); for(int i=0;i<k1;i++)
{
String k=sc.nextLine(); String s=sc.nextLine(); hm.put(k,s);
}
String n=sc.nextLine();
LinkedHashMap<String,String> hm1=new LinkedHashMap<String,String>(); hm1=UserMainCode.obtainDesignation(hm,n);
Iterator<String> it=hm1.keySet().iterator(); while(it.hasNext())
{
 
String s2=it.next(); System.out.println(s2);
}
}
}




import java.util.HashMap; import java.util.Iterator;
import java.util.LinkedHashMap; import java.util.Map;
import java.util.Scanner; public class UserMainCode
{
public static LinkedHashMap<String,String> obtainDesignation(LinkedHashMap<String,String> h1,String n)
{
int k=0;
LinkedHashMap<String,String> hm1=new LinkedHashMap<String,String>(); Iterator<String>it=h1.keySet().iterator();
while(it.hasNext())
{
String s2=it.next(); String s3=h1.get(s2); if(s3.equals(n))
hm1.put(s2,s3);
}
return hm1;
 
}}




	Grade Calculator



import java.util.Iterator;
import java.util.LinkedHashMap; import java.util.Scanner;
public class Main {
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in); int k1=Integer.parseInt(sc.nextLine());
LinkedHashMap<String,String> hm=new LinkedHashMap<String,String>(); for(int i=0;i<k1;i++)
{
 
String k=sc.nextLine(); String s=sc.nextLine(); hm.put(k,s);
}
String n=sc.nextLine();
LinkedHashMap<String,String> hm1=new LinkedHashMap<String,String>(); hm1=UserMainCode.obtainDesignation(hm,n);
Iterator<String> it=hm1.keySet().iterator(); while(it.hasNext())
{
String s2=it.next(); System.out.println(s2);
}
}
}
import java.util.HashMap; import java.util.Iterator;
import java.util.LinkedHashMap; import java.util.Map;
import java.util.Scanner; public class UserMainCode
{
public static LinkedHashMap<String,String> obtainDesignation(LinkedHashMap<String,String> h1,String n)
{
int k=0;
LinkedHashMap<String,String> hm1=new LinkedHashMap<String,String>(); Iterator<String>it=h1.keySet().iterator();
 
while(it.hasNext())
{
String s2=it.next(); String s3=h1.get(s2); if(s3.equals(n))
hm1.put(s2,s3);
}
return hm1;
}}


 DOB - Validation


import java.text.SimpleDateFormat; import java.util.Date;
import java.util.Scanner; public class Main {
public static void main(String[] args)
{
String str=new String();
Scanner sc=new Scanner(System.in); str=sc.nextLine();
Boolean b=UserMainCode.ValidateDOB(str); if(b==”true”)
System.out.println("TRUE"); if(b==”false”)
System.out.println("FALSE");
}
}


import java.text.SimpleDateFormat; import java.util.Date;
public class UserMainCode {
public static Boolean ValidateDOB(String str){
 
Boolean b=”false”;
SimpleDateFormat sdf=new SimpleDateFormat("MM/dd/yyyy"); sdf.setLenient(false);
try
{
Date d1=sdf.parse(str); return b=”true”;
}
catch(Exception e)
{
return b=”false”;
}

}
}
	Experience Validator


import java.util.ArrayList; import java.util.HashMap; import java.util.Scanner; public class Main {
public static void main(String args[]){ Scanner sc = new Scanner(System.in); String s=sc.nextLine();
String s1=sc.nextLine(); System.out.println(UserMainCode.validateExp(s,s1));
}
}


import java.util.Calendar; import java.util.Date;
public class UserMainCode {
public static boolean validateExp(String s,String s1)
 
{
int y1=Integer.parseInt(s); Date d=new Date();
Calendar c=Calendar.getInstance(); int y2=c.get(Calendar.YEAR);
int y=Math.abs(y1-y2);
int e=Integer.parseInt(s1); if(y>=e)
return true; else
return false;
}}
	ArrayList to String Array


import java.util.*;

public class Main

{

public static void main(String[] args)

{

Scanner s=new Scanner(System.in);

ArrayList<String> l=new ArrayList<String>();

int n=s.nextInt();

for(int i=0;i<n;i++)

{

l.add(s.next());
 
}

String a[]=new String[n]; a=UserMainCode.convertToStringArray(l); for(int j=0;j<n;j++)
{

System.out.println(a[j]);

}

}

}



import java.util.ArrayList;

import java.util.Collections;



class UserMainCode

{

public static String[] convertToStringArray(ArrayList<String> l)

{

Collections.sort(l);

String [] a = l.toArray(new String[l.size()]);

return a;

}

}



	State ID generator
 
 
String[] s1=new String[n];

for(int i=0;i<n;i++)

{

s1[i]=s.next();

}

HashMap<String, String> hm = new HashMap<String, String>();

hm = UserMainCode.putvalues(s1);

for(Map.Entry<String, String> ans: hm.entrySet())

{

System.out.println(ans.getKey()+":"+ans.getValue());

}

}}

User main code



import java.util.ArrayList;
import java.util.HashMap;
import java.util.Map;
public class UserMainCode{
public static HashMap<String, String> putvalues(String[] s1)

{

HashMap<String, String> hm = new HashMap<String, String>();

ArrayList<String> lst1 = new ArrayList<String>();

ArrayList<String> lst2 = new ArrayList<String>();

}

	ArrayList to String Array
USERMAINCODE:


import java.util.ArrayList;

import java.util.*;

public class UserMainCode {
 
public static String[] fruitSelector(ArrayList<String> a1,ArrayList<String> a2)

{

ArrayList<String> a3=new ArrayList<String>();

for(int i=0;i<a1.size();i++)

{

String s1=a1.get(i);

if(s1.charAt(s1.length()-1)!='a'&&s1.charAt(s1.length()-1)!='e'&&s1.charAt(s1.length()- 1)!='A'&&s1.charAt(s1.length()-1)!='E')

{

a3.add(s1);

}

}

ArrayList<String> a4=new ArrayList<String>();

for(int j=0;j<a2.size();j++)

{

String s2=a2.get(j);

if(s2.charAt(0)!='m'&&s2.charAt(0)!='a'&&s2.charAt(0)!='M'&&s2.charAt(0)!='A')

{

a4.add(s2);

}

}

a3.addAll(a4); Collections.sort(a3);
String st[]=new String[a3.size()];

for(int k=0;k<a3.size();k++)

{

st[k]=a3.get(k);

}

return st;
 
}

}



MAIN:

import java.util.*;

import java.util.ArrayList;

public class Main {

public static void main(String [] args)

{

Scanner s=new Scanner(System.in);

int m=s.nextInt();

ArrayList<String> aa1=new ArrayList<String>();

for(int i=0;i<m;i++)

{

aa1.add(s.next());

}

int n=s.nextInt();

ArrayList<String> aa2=new ArrayList<String>();

for(int j=0;j<n;j++)

{

aa2.add(s.next());

}

int k;

String st[]=UserMainCode.fruitSelector(aa1,aa2);

for( k=0;k<st.length;k++)

{

System.out.println(st[k]);

}

if(st.length==0)
 
System.out.println("No Fruit Found"); s.close();
}

}

Elements in ArrayList

MAIN:
import java.util.*;
public class Main
{
public static void main(String[] args)
{
int n,m;
Scanner sin = new Scanner(System.in); n = sin.nextInt();
ArrayList<Integer> a1 = new ArrayList<Integer>(n);
for(int i=0;i<n;i++)
{
int k = sin.nextInt(); a1.add(k);
}
m = sin.nextInt();
ArrayList<Integer> a2 = new ArrayList<Integer>(m);
for(int i=0;i<m;i++)
{
int k = sin.nextInt(); a2.add(k);
}
int[] result = UserMainCode.arrayListSubtractor(a1,a2); Arrays.sort(result);
for(int i=0;i<result.length;i++) System.out.println(result[i]);
}
}
USERMAINCODE:
import java.util.ArrayList;
public class UserMainCode
{
public static int[] arrayListSubtractor(ArrayList<Integer> arrlist1,ArrayList<Integer>
arrlist2)
{
int count=0,key;
int max = arrlist1.size(); if(arrlist1.size() < arrlist2.size()) max = arrlist2.size();
ArrayList<Integer> temp = new ArrayList<Integer>(max);
for(int i=0;i<arrlist1.size();i++)
{
key = (int)arrlist1.get(i);
if(arrlist2.indexOf(key) == -1)
{
++count; temp.add(key);
}
}
for(int i=0;i<arrlist2.size();i++)
{
key = (int)arrlist2.get(i);
if(arrlist1.indexOf(key) == -1)
 
{
if(!temp.contains(key))
{
++count; temp.add(key);
}
}
}
int[] result = new int[count]; for(int i=0;i<count;i++) result[i] = (int)temp.get(i); return result;
}
}

Price Calculator - II

MAIN:
import java.util.HashMap;
import java.util.Scanner;


public class Main {
public static void main(String[] args) { Scanner S=new Scanner(System.in); int n=S.nextInt();

HashMap<String, Float> m1=new HashMap<String, Float>();
for(int i=0;i<n;i++)
{
String name=S.next(); float price=S.nextFloat(); m1.put(name,price);
}
int m=S.nextInt();
String s[]=new String[m];
for(int j=0;j<m;j++)
{
s[j]=S.next();
}
System.out.println(UserMainCode.getTheTotalCostOfPheripherals
(m1,s));
}
}
USERMAINCODE:
import java.util.HashMap;
import java.util.Iterator;


public class UserMainCode {
public static float getTheTotalCostOfPheripherals(HashMap<String,Float> m1, String[] s) {
Float f=(float) 0;
Iterator<String> i=m1.keySet().iterator();
while(i.hasNext()){ String s1=i.next(); Float f1=m1.get(s1);
for(int j=0;j<s.length;j++)
if(s[j].equals(s1)) f+=f1; }
return f;
}
}

	String Processing - ZigZag

MAIN:
import java.io.BufferedReader;
import java.io.IOException; import java.io.InputStreamReader; import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.*;
public class Main {
public static void main(String[] args) throws IOException, ParseException {
Scanner S=new Scanner(System.in); String s1=S.next(); UserMainCode.getLastDayOfMonth(s1);
}
}
USERMAINCODE:
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.Calendar;
import java.util.Date;


public class UserMainCode {
public static void getLastDayOfMonth(String s1) throws ParseException{ SimpleDateFormat sdf=new SimpleDateFormat("dd-MM-yyyy");
Calendar cal=Calendar.getInstance(); Date d1=sdf.parse(s1); cal.setTime(d1);
int n=cal.getActualMaximum(Calendar.DAY_OF_MONTH); System.out.println(n);
}
}


	Leap Year

MAIN:
import java.io.IOException;
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.*;
public class Main {
public static void main(String[] args) throws IOException, ParseException { Scanner S=new Scanner(System.in);
String s1=S.next(); UserMainCode.isLeapyear(s1);
}
}
USERMAINCODE:
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.Date;
import java.util.GregorianCalendar;
import java.util.StringTokenizer;


public class UserMainCode {
public static void isLeapyear(String s1) throws ParseException{ SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); GregorianCalendar g=new GregorianCalendar();
StringTokenizer t=new StringTokenizer(s1,"/"); String s2=t.nextToken();
String s3=t.nextToken(); String s4=t.nextToken();
int n1=Integer.parseInt(s4); Date d1=sdf.parse(s1); boolean b=g.isLeapYear(n1); System.out.println(b);
}
}

Largest Chunk

MAIN:
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner S=new Scanner(System.in); String s1=S.nextLine();
System.out.println(UserMainCode.getLargestSpan(s1));
}
}
USERMAINCODE:
import java.util.StringTokenizer;


public class UserMainCode {
public static int getLargestSpan(String s1) {
int max=0;
StringTokenizer t=new StringTokenizer(s1," ");
while(t.hasMoreTokens()){ String s2=t.nextToken(); int n=0;
for(int i=0;i<s2.length()-1;i++) if(s2.charAt(i)==s2.charAt(i+1)) n++;
if(n>max) max=n;
}
return (max+1);
} }

	Largest Span

MAIN:
import java.util.Scanner;
public class Main {
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in);
int n=sc.nextInt(); int []a=new int[n]; for(int i=0;i<n;i++)
{
a[i]=sc.nextInt();
}
System.out.print(UserMainCode.getLargestSpan(a,n));
}}

USERMAINCODE:
public class UserMainCode {
public static int getLargestSpan(int[] x,int n)
{
int gap=0,max=0;
for(int i=0;i<n;i++)
{
for(int j=i+1;j<n;j++)
{
if(x[i]==x[j])
{
gap=j;
}
}
if(gap-i>max) max=gap-i;
}
return max+1;
}
}

Even Sum & Duplicate Elements

MAIN:
import java.util.HashMap; import java.util.LinkedHashMap; import java.util.LinkedHashSet; import java.util.Scanner; public class Main
{
public static void main(String args[])
{
Scanner sc=new Scanner(System.in);
int n=sc.nextInt(); int a[]=new int[n]; for(int i=0;i<n;i++)
{
a[i]=sc.nextInt();
}
System.out.println(UserMainCode.sumElements(a));
}}
 
USERMAINCODE:
import java.util.Iterator; import java.util.LinkedHashSet; public class UserMainCode {
public static int sumElements(int a[])
{
LinkedHashSet<Integer>h1=new LinkedHashSet<Integer>();
int s=0;
for(int i=0;i<a.length;i++)
{
h1.add(a[i]);
}
Iterator<Integer> it=h1.iterator();
while(it.hasNext())
{
int k=it.next();
if(k%2==0)
{
s=s+k;
}
}
if(s>0) return s; else return -1;
}
}




Regular Expression - III

Main:
import java.util.Scanner;
 

public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String a=s.next();
System.out.println(UserMainCode.passwordValidation(a)); s.close();
}
}
UserMainCode:
public class UserMainCode
{
public static String passwordValidation(String a)
{
String k; if(a.matches(".*[0-
9]{1,}.*")&&a.matches(".*[@#$]{1,}.*")&&a.length()>=8&&a.matches(".*[A- Z]{1,}.*")&&a.matches(".*[a-z].*"))
{
k="validinput";
}
else
{
k="Invalidinput";
}
return k;
}

}

	Integer Factorial
Main:
import java.util.Iterator;
import java.util.LinkedHashMap; import java.util.Scanner;
public class Main
{
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); int a=Integer.parseInt(s.nextLine());; int[]k=new int[a];
for(int i=0;i<a;i++)
{
k[i]=s.nextInt();
}
LinkedHashMap<Integer,Integer>hm=new LinkedHashMap<Integer,Integer>(); hm=UserMainCode.getFactorial(k);
Iterator<Integer> it=hm.keySet().iterator(); for(int i=0;i<a;i++)
{
int n=it.next();
int fac=hm.get(n); System.out.println(n+":"+fac); s.close();
}
}
}
UserMainCode;
import java.util.LinkedHashMap;


public class UserMainCode
{
public static LinkedHashMap<Integer,Integer> getFactorial(int[] k)
{
LinkedHashMap<Integer,Integer> hm1=new LinkedHashMap<Integer,Integer>(); for(int i=0;i<k.length;i++)
{
int u=1;
for(int j=1;j<=k[i];j++)
{
u=u*j; 
}
hm1.put(k[i],u);
}
return hm1;
}
}
	String processing – Long + Short + Long

Main;
import java.util.Scanner;
public class Main
{
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String s1=s.next();
String s2=s.next(); System.out.println(UserMainCode.getCombo(s1,s2)); s.close();
}
}
UserMainCode;
public class UserMainCode
{
public static String getCombo(String s1,String s2)
{
StringBuffer sb=new StringBuffer(); int p=s1.length();
int q=s2.length(); if(p>q)
 
{
sb.append(s1).append(s2).append(s1);
}
else
{
sb.append(s2).append(s1).append(s2);
}
return sb.toString();
}
}

	Age for Voting

Main:
import java.util.Scanner;


public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String a=s.nextLine();
System.out.println(UserMainCode.getAge(a)); s.close();
}
}
UserMainCode:
import java.text.SimpleDateFormat; import java.util.Date;
import java.util.Scanner;


public class UserMainCode
{
public static String getAge(String n)
{
 
Scanner s=new Scanner(System.in); int year=0;
String s1=s.next();
SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); try
{
Date d=sdf.parse(n); Date d1=sdf.parse(s1); int y=d.getYear();
int y1=d1.getYear(); int m=d.getMonth(); int m1=d1.getMonth(); int day=d.getDate(); int day1=d1.getDate(); year=y1-y;
if(m>m1) year--;
else if(m==m1)
{if(day<day1) year--;
}
}
catch(Exception e)
{
e.printStackTrace();
}
if(year>18) return "eligible"; else
return "not-eligible";
}
}

	Unique Even Sum

Main:

import java.util.Scanner;
public class Main
{
public static void main(String[] args)
{
Scanner s=new Scanner(System.in);
int n=s.nextInt(); int[] a=new int [n]; for(int i=0;i<n;i++)
{
a[i]=s.nextInt();
}
System.out.println(UserMainCode.addUniqueEven(a)); s.close();
}

}
UserMainCode;


import java.util.Iterator;
import java.util.LinkedHashSet;
public class UserMainCode
{
public static int addUniqueEven(int[] a)
 
{
int sum=0;
LinkedHashSet<Integer> hm=new LinkedHashSet<Integer>();
for(int i=0;i<a.length;i++)
{
hm.add(a[i]);
}
Iterator<Integer> im=hm.iterator();
while(im.hasNext())
{
int b=im.next(); if(b%2==0) sum=sum+b;
}
if(sum>0)
{
return sum;
}
else
return -1;
}
}

	Palindrome & Vowels

Main;
import java.util.Scanner;
 
public class Main
{
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in); String s=sc.nextLine();
System.out.println(UserMainCode.checkPalindrome(s)); sc.close();
}
}
UserMainCode;
import java.util.Iterator;
import java.util.LinkedHashSet;

public class UserMainCode
{
public static int checkPalindrome(String s)
{
StringBuffer sb=new StringBuffer(s); int k=0;
LinkedHashSet<Character>l1=new LinkedHashSet<Character>(); String s2=sb.reverse().toString();
if(s2.equals(s))
{
String s3=s2.toLowerCase(); for(int i=0;i<s3.length();i++)
{
l1.add(s3.charAt(i));
}
Iterator<Character> it=l1.iterator(); while(it.hasNext())
{
char a=it.next(); if(a=='a'||a=='e'||a=='i'||a=='o'||a=='u') k++;
}
}
if(k>=2) return 1; else return -1;
}

}

	Strings – Unique & Existing Characters
Main;
import java.util.Scanner;


public class Main
{
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in); String s=sc.next();
String s1=sc.next(); System.out.println(UserMainCode.replacePlus(s,s1)); sc.close();
}

}
UserMainCode;

public class UserMainCode
{
public static String replacePlus(String s,String s1)
{
{
String s2=s.toLowerCase(); String s3=s1.toLowerCase();
 
StringBuffer sb=new StringBuffer(); for(int i=0;i<s.length();i++)
{
char c=s2.charAt(i); if(s3.indexOf(c)==-1) sb.append("+");
else sb.append(s.charAt(i));
} return sb.toString();
}
}

}


Longest Word
Main;
import java.util.Scanner;


public class Main
{
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String s1=s.nextLine();
System.out.println(UserMainCode.getLargestWord(s1)); s.close();
}
 
}
UserMainCode;

import java.util.StringTokenizer;


public class UserMainCode
{
public static String getLargestWord(String s1)
{
int max=0;
String s2=new String();
StringTokenizer t=new StringTokenizer(s1," ");
{
while(t.hasMoreTokens()){ String s3=t.nextToken(); int n=s3.length(); if(n>max){
max=n; s2=s3;}
}
return s2;
}
}
}


String Occurences

UserMainCode

import java.util.StringTokenizer;

public class UserMainCode
{
public static void countNoOfWords(String s1, String s2) {
int count=0;

StringTokenizer st=new StringTokenizer(s2," "); String s3=st.nextToken();
String s4=st.nextToken();

//System.out.println(s4);

StringTokenizer st1=new StringTokenizer(s1," ");

while(st1.hasMoreTokens())

{

String s5=st1.nextToken();

if(s4.equals(s5))
{
count++;
}
}

System.out.println(count);
}
}

Main
import java.util.*;

public class Main

{

/**

* @param args

*/

public static void main(String[] args)

{
Scanner s=new Scanner(System.in); String s1=s.nextLine();
String s2=s.nextLine(); UserMainCode.countNoOfWords(s1,s2); s.close();
}
}



ArrayList Manipulation

UserMainCode
import java.util.ArrayList;

import java.util.Iterator;

public class UserMainCode

{

public static ArrayList<Integer> generateOddEvenList (ArrayList<Integer>al1,ArrayList<Integer>al2)

{

ArrayList<Integer>al3=new ArrayList<Integer>();

for(int i=0;i<al1.size();i++)

{

if(i%2==0) al3.add(al2.get(i)); else al3.add(al1.get(i));
}
return al3;
}
 
}

Main

import java.util.ArrayList; import java.util.Iterator; import java.util.Scanner; public class Main {
public static void main(String []args){ Scanner sc=new Scanner(System.in);
int s=Integer.parseInt(sc.nextLine()); ArrayList<Integer>al1=new ArrayList<Integer>(); ArrayList<Integer>al2=new ArrayList<Integer>(); for(int i=0;i<s;i++)
al1.add(sc.nextInt()); for(int i=0;i<s;i++) al2.add(sc.nextInt());
ArrayList<Integer>al3=new ArrayList<Integer>(); al3=UserMainCode.generateOddEvenList(al1,al2); Iterator<Integer> it=al3.iterator(); while(it.hasNext())
{
int n=it.next(); System.out.println(n); sc.close();
}
} 
}

	Duplicate Characters

UserMainCode

import java.util.HashSet;
import java.util.Iterator;
import java.util.LinkedHashSet;
import java.util.StringTokenizer;
public class UserMainCode
{
public static void removeDuplicates(String s1) {
char a[]=s1.toCharArray(); StringBuffer sb=new StringBuffer();
LinkedHashSet<Character>hs=new LinkedHashSet<Character>();
for(int i=0;i<a.length;i++)
{
hs.add(a[i]);
}

Iterator<Character>itr=hs.iterator();

while(itr.hasNext())

{

char o=itr.next();

if(o!=' ');

{
sb.append(o);
}

}

System.out.println(sb);

}

}

Main
import java.util.*;
 public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); String s1=s.nextLine(); UserMainCode.removeDuplicates(s1); s.close();
}
}
Mastering Hashmap
UserMainCode
import java.util.HashMap;
import java.util.Scanner;
import java.util.HashMap;
import java.util.Iterator;
public class UserMainCode {
public static int getAverageOfOdd(HashMap<Integer,Integer>h1)
{
int av=0,c=0,s=0;
Iterator<Integer> it=h1.keySet().iterator();
while(it.hasNext())
{
int a=it.next();
if(a%2!=0)
{
int b=h1.get(a);
s=s+b; c++;
}
}
av=s/c;
return av;
}}
Main
import java.util.*;
public class Main
{
public static void main(String args[])
{
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
HashMap<Integer,Integer> h1=new HashMap<Integer,Integer>();
for(int i=0;i<n;i++)
{
h1.put(sc.nextInt(),sc.nextInt());
}
System.out.println(UserMainCode.getAverageOfOdd(h1)); sc.close();
}
}
 Managers & Hashmaps
UserMainCode
import java.util.HashMap; import java.util.Iterator; import java.util.HashMap;
public class UserMainCode
{
public static HashMap<Integer,Integer> display(HashMap<Integer,String>hm,HashMap<Integer,Integer>hm1)
{
HashMap<Integer,Integer>hm3=new HashMap<Integer,Integer>(); Iterator<Integer> it=hm.keySet().iterator(); while(it.hasNext())
{
int id=it.next(); String name=hm.get(id);
if(name.equals("manager"))
{
	int salary=hm1.get(id)+5000; hm3.put(id,salary);
}}
return hm3;
}
}
Main
import java.util.HashMap; import java.util.Iterator; import java.util.Scanner; public class Main {
public static void main(String []args){
 Scanner sc=new Scanner(System.in);
int s=Integer.parseInt(sc.nextLine()); HashMap<Integer,String>hm=new HashMap<Integer,String>(); HashMap<Integer,Integer>hm1=new HashMap<Integer,Integer>(); for(int i=0;i<s;i++)
{
int id=Integer.parseInt(sc.nextLine()); hm.put(id, sc.nextLine()); hm1.put(id,Integer.parseInt(sc.nextLine()));
}
HashMap<Integer,Integer>hm2=new HashMap<Integer,Integer>(); hm2=UserMainCode.display(hm,hm1);
Iterator<Integer> it=hm2.keySet().iterator();
while(it.hasNext())
{
int n=it.next();
int fac=hm2.get(n); System.out.println(n); System.out.println(fac);
}
}
}
	Check first and last word
UserMainCode
import java.util.StringTokenizer;
public class UserMainCode
{
public static int check(String s)
{
int count=0; String fin="";
StringTokenizer st=new StringTokenizer(s); String ini=st.nextToken(); while(st.hasMoreTokens())
{ fin=st.nextToken();
}
 if(ini.equals(fin)) count=ini.length(); else
count=ini.length()+fin.length();
return count;
}
}
Main
import java.util.HashMap;
import java.util.Iterator;
import java.util.Scanner;
public class Main {
public static void main(String []args){ Scanner sc=new Scanner(System.in); String age=sc.nextLine();
System.out.println(UserMainCode.check(age)); sc.close();
}}
Concatenate Characters
UserMainCode
public class UserMainCode
{
public static String concatCharacter(String[] a)
{
StringBuffer sb=new StringBuffer(); for(int i=0;i<a.length;i++) sb.append(a[i].charAt(a[i].length()-1)); return sb.toString();
}
}
Main
import java.util.*;
public class Main
{
public static void main(String []args){ Scanner sc=new Scanner(System.in);
int s=Integer.parseInt(sc.nextLine()); String []a=new String[s];
for(int i=0;i<s;i++)
{
a[i]=sc.nextLine();
}
System.out.println(UserMainCode.concatCharacter(a)); sc.close();
}
}
12.	Anagram
UserMainCode
import java.util.ArrayList; import java.util.Collections; import  java.util.List; import java.util.Scanner;
public class UserMainCode
{
public static void getAnagram(String s1,String s2)
{
List<Character> l1=new ArrayList<Character>();
 List<Character> l2=new ArrayList<Character>(); String s3=s1.replace(" ","");
String s4=s2.replace(" ",""); String s5=s3.toUpperCase(); String s6=s4.toUpperCase();
for (int i = 0; i < s5.length(); i++)
{
l1.add(s5.charAt(i));
}
for (int i = 0; i < s6.length(); i++)
{
l2.add(s6.charAt(i));
}
Collections.sort(l1); Collections.sort(l2);
// System.out.println(l1);

// System.out.println(l2); if(l1.equals(l2)) System.out.println("Anagram"); else
System.out.println("Not Anagram");
}
}
Main
import java.util.ArrayList;
 import java.util.Collections;
import java.util.List;
import java.util.Scanner;
public class Main{
public static void main(String[] args)
{
Scanner sc =new Scanner(System.in);
String s1=sc.nextLine(); String s2=sc.nextLine();
UserMainCode.getAnagram(s1,s2);
}
}
	Calculate Meter Reading
import java.util.Scanner;
public class Main{
public static void main (String[] args)
{
// your code goes here
Scanner sc = new Scanner(System.in);
 String input1=sc.next(); String input2=sc.next();
System.out.println(UserMainCode.calculateMeterReading(input1,input2)); sc.close();
}}
public class UserMainCode {
public static int calculateMeterReading(String input1, String input2)
{
int n1=Integer.parseInt(input1.substring(5,input1.length())); int n2=Integer.parseInt(input2.substring(5,input2.length())); int n=Math.abs((n2-n1)*4);
return n;
}
}
	Retirement
import java.text.ParseException; import java.util.LinkedHashMap; import  java.util.Scanner; public class Main
{
public static void main(String args[]) throws ParseException{ Scanner sc=new Scanner(System.in); int
n=Integer.parseInt(sc.nextLine());
LinkedHashMap<String,String>a1=new LinkedHashMap<String,String>(); for(int
i=0;i<n;i++) { a1.put(sc.nextLine(),sc.nextLine());
}
System.out.println(UserMainCode.retirementEmployeeList(a1));
}
}
import java.text.*;
import java.util.*;
public class UserMainCode {
 
public static ArrayList<String> retirementEmployeeList(LinkedHashMap<String,String>a1) throws ParseException
{
ArrayList<String>al=new ArrayList<String>(); Iterator <String>it=a1.keySet().iterator(); while(it.hasNext())
{String s=it.next(); String s1=a1.get(s);
SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); sdf.setLenient(false);
try{
Date d=new Date(); Date d1=new Date(); String a=s1;
String b="01/01/2014"; d=sdf.parse(a); d1=sdf.parse(b);
long t=d.getTime(); long t1=d1.getTime(); long t3=t1-t;
long l1=(24 * 60 * 60 * 1000);
long l=l1*365; long res=t3/l; if(res>=60)
{
al.add(s);
}
}
catch (Exception e) { e.printStackTrace();
}
}
Collections.sort(al);
return al;
}
}
	Kaprekar Number
import java.util.*;
public class Main{
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
int v=UserMainCode.getKaprekarNumber(n);
if (v==1)
System.out.println("Kaprekar Number");
else
System.out.println("Not a Kaprekar Number");
}}
public class UserMainCode {
public static int getKaprekarNumber(int a)
{
int count=0,j=0; int a1=a; while(a1!=0)
{
count=count+1; a1=a1/10;
}
int square=a*a;
String s=Integer.toString(square); String s1=s.substring(0,count); String s2=s.substring(count);
int x=Integer.parseInt(s1); int y=Integer.parseInt(s2); int result =x+y; if(result==a){
j=1;
}
else
{ j=2;
}
return j;
}}
	Vowels
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner sc=new Scanner(System.in);
String s1 =sc.nextLine(); UserMainCode.storeMaxVowelWord(s1);
}
}
import java.util.StringTokenizer;
public class UserMainCode {
public static void storeMaxVowelWord(String s1) {
int i = 0;
StringTokenizer st = new StringTokenizer(s1," ");
int len = 0; int count = 0; int count2 = 0;
String s6 = null;
while (st.hasMoreTokens()) { String s5 = st.nextToken(); len = s5.length();
count=0;
for (i = 0; i < len; i++) {
if (s5.charAt(i) == 'a' || s5.charAt(i) == 'e'|| s5.charAt(i) == 'i'
|| s5.charAt(i) == 'o'|| s5.charAt(i) == 'u'
||s5.charAt(i) == 'A' ||s5.charAt(i) == 'E' ||s5.charAt(i) == 'I'
||s5.charAt(i) == 'O' ||s5.charAt(i) == 'U')
count++;
}
if (count > count2)
{
count2 = count; s6 = s5;
}
}
System.out.println(s6);
}
}

	Unique Characters REPEATED

import java.util.*;
public class Main
{
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in); String s1=sc.next(); UserMainCode.checkUnique(s1);
}
}
import java.util.*;
public class UserMainCode {

public static void checkUnique(String s1)
{
String s2=s1.toLowerCase(); StringBuffer sb=new StringBuffer(s2); int l=sb.length();
int count=0;
for(int i=0;i<l;i++)
{ count=0;
for(int j=i+1;j<l;j++)
{
if(sb.charAt(i)==sb.charAt(j))
{
sb.deleteCharAt(j); count++;
j--;
l--;
}
}
if(count>0)
{
sb.deleteCharAt(i); i--;
l--;
}
}
if(sb.length()==0)
{
System.out.println(-1);
}
else
System.out.println(sb.length());
}
}
 
	average of primes

import java.util.Scanner;
public class Main{
public static void main (String[] args)
{
// your code goes here
Scanner sc = new Scanner(System.in);
int n = sc.nextInt(); System.out.println(UserMainCode.addPrimeIndex(n));
}}
import java.util.*;
public class UserMainCode {
public static int addPrimeIndex(int n) { Scanner sc=new Scanner(System.in); int[] a = new int[n];
for(int i=0;i<n;i++){ a[i] = sc.nextInt();
}
int sum=0;
int count=0;
int sum_count=0;
for(int i=0;i<a.length;i++)
{
count=0;
for(int j=1;j<=i;j++)
{
if(i%j==0)
{
count++;
}
}
if(count==2)
{
sum=sum+a[i]; sum_count++;
}
}
int avg=sum/sum_count;
return avg;
}}
 
	ArrayList and Set Operations
Main:
 import java.util.ArrayList; import java.util.Scanner; public class Main {
public static void main(String args[]){ Scanner sc = new Scanner(System.in); int n=Integer.parseInt(sc.nextLine());
ArrayList<Integer>a1=new ArrayList<Integer>(); ArrayList<Integer>a2=new ArrayList<Integer>(); for(int i=0;i<n;i++) a1.add(Integer.parseInt(sc.nextLine()));
for(int i=0;i<n;i++) a2.add(Integer.parseInt(sc.nextLine())); char c=sc.nextLine().charAt(0);
System.out.println(UserMainCode.performSetOperations(a1,a2,c));
}
}
UserMainCode:
import java.util.ArrayList; import java.util.ArrayList;
public class UserMainCode {
public static ArrayList<Integer> performSetOperations(ArrayList<Integer>a1,ArrayList<Integer>a2,char c)
{
ArrayList<Integer>op1=new ArrayList<Integer>(); int k=0;
switch(c)
{
case '+': a1.removeAll(a2);
 
a1.addAll(a2); op1=a1; break;
case '*': a1.retainAll(a2); op1=a1;
break; case '-':
for(int i=0;i<a1.size();i++)
{ k=0;
for(int j=0;j<a2.size();j++)
{
if(a1.get(i)==a2.get(j)) k=1;
}
if(k==0) op1.add(a1.get(i));
}
break;
}
return op1;
}}
}
return tm;
}
 }

	Largest Span

MAIN:
import java.util.Scanner;
public class Main {
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in);
int n=sc.nextInt(); int []a=new int[n]; for(int i=0;i<n;i++)
{
a[i]=sc.nextInt();
}
System.out.print(UserMainCode.getMaxSpan(a,n));
}}
USERMAINCODE:
class UserMainCode {
public static int getMaxSpan(int[] x,int n)
{
int gap=0,max=0;
for(int i=0;i<n;i++)
{
for(int j=i+1;j<n;j++)
{
if(x[i]==x[j])
 
gap=j;
}
if(gap-i>max) max=gap-i;
}
return max+1;
}
}
	Max Scorer
USERMAINCODE:
import java.util.ArrayList; import java.util.StringTokenizer; public class UserMainCode
{
public static String highestScorer(ArrayList<String>s1)
{
int max=0; String s4=null;
for(int i=0;i<s1.size();i++)
{
String s2=s1.get(i);
StringTokenizer t=new StringTokenizer(s2,"-");
 String s3=t.nextToken();
int n1=Integer.parseInt(t.nextToken()); int n2=Integer.parseInt(t.nextToken()); int n3=Integer.parseInt(t.nextToken()); int n=n1+n2+n3;
if(n>max)
{
max=n; s4=s3;
}
}
return s4;
}
}
MAIN:
import java.util.*;
public class Main {
public static void main(String[] args) {
// TODO Auto-generated method stub Scanner s=new Scanner(System.in);
int n=s.nextInt();
ArrayList<String> s1=new ArrayList<String>();
for(int i=0;i<n;i++)
{
s1.add(s.next());
}
System.out.println(UserMainCode.highestScorer(s1)); s.close();

}
}
	Max Vowels
USERMAINCODE:
import java.util.StringTokenizer;
public class UserMainCode {
public static String getWordWithMaximumVowels(String s1)
{
int i;
StringTokenizer t=new StringTokenizer(s1," ");
int count=0,max=0; String s2=null; while(t.hasMoreTokens())
{
String s3=t.nextToken(); count=0; for(i=0;i<s3.length();i++)
{
if(s3.charAt(i)=='a'||s3.charAt(i)=='e'||s3.charAt(i)=='i'||s3.charAt(i)==' o'||s3.charAt(i)=='u'
||s3.charAt(i)=='A'||s3.charAt(i)=='E'||s3.charAt(i)=='I'||s3.charAt(i)=='O '||s3.charAt(i)=='U')
count++;
}
if(count>max)
{
	
	
 }
}
MAIN:
 


}

}
return s2;
 
max=count; s2=s3;
 

import java.util.*;
public class Main {

public static void main(String[] args) {
// TODO Auto-generated method stub Scanner s=new Scanner(System.in);
String s1=s.nextLine(); System.out.println(UserMainCode.getWordWithMaximumVowels(s1)); s.close();
}

}
or
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.*;

public class Main {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);
String s1 = sc.nextLine();
int max = 0;
String s4 = "";
StringTokenizer st = new StringTokenizer(s1, " ");
while (st.hasMoreTokens()) {
String s2 = st.nextToken();
String s3 = s2.replaceAll("[aeiouAEIOU]", "");
int len = s3.length();
if (len > max) {
max = len;
s4 = s2;
}
}
System.out.println(s4);
}
}
or
import java.util.Scanner;
publicclass Main {

	publicstaticvoid main(String[] args) {
		
		Scanner sc=new Scanner(System.in);
		
		String s=sc.nextLine();
		
		System.out.println(UserMainCode.getstring(s));
	}}
publicclass UserMainCode {
	publicstatic String getstring(String s) 
	{   
		int m=0;
		String op="";
		StringTokenizer st=new StringTokenizer(s," ");
		while(st.hasMoreTokens())
		{
			String v=st.nextToken();
			String r=v;
			r=r.replaceAll("[aeiouAEIOU]", "");
			if(m<(v.length()-r.length()))
			{
				m=v.length()-r.length();
				op=v;
			}
		}
		return op;
}
}



	All Vowels
 
public class UserMainCode {
public static int getOrderVowels(String s1)
{

String s2="aeiou";
StringBuffer sb=new StringBuffer();
for(int i=0;i<s1.length();i++)
{
for(int j=0;j<s2.length();j++)
{
if(s1.charAt(i)==s2.charAt(j))
{
sb.append(s1.charAt(i));
}
}
}
if(sb.toString().equals(s2))
{
return 1;
}
return -1;
}
}
MAIN:

import java.util.*;
public class Main {

public static void main(String[] args) {
// TODO Auto-generated method stub Scanner s=new Scanner(System.in);
String s1=s.next();
 
int b=UserMainCode.getOrderVowels(s1);
if(b==1)
{
 

}
else
 
System.out.println("Valid");


System.out.println("Invalid");
 
s.close();
}

}

	Adjacent Swaps

import java.util.*;
public class UserMainCode {
public static String swapPairs(String s1)
{
int i;
StringBuffer sb=new StringBuffer();
for(i=0;i<s1.length()-1;i=i+2)
{
if(i%2==0)
{
 



}
else

{
 
char a=s1.charAt(i); char b=s1.charAt(i+1); sb.append(b).append(a);

for(i=0;i<s1.length()-1;i=i+2) char a=s1.charAt(i);
char b=s1.charAt(i+1);
 
sb.append(b).append(a); sb.append(s1.charAt(s1.length()-1));
}

 


}
}
MAIN:
 
}
return sb.toString();
 

import java.util.*;
public class Main {

public static void main(String[] args) {
// TODO Auto-generated method stub Scanner s=new Scanner(System.in);
String s1=s.nextLine(); System.out.println(UserMainCode.swapPairs(s1)); s.close();
}

}

	Sum of Digits
USERMAINCODE:
public class UserMainCode {
public static int getDigits(String s1)
{
int sum=0;
for(int i=0;i<s1.length();i++)
{
char a=s1.charAt(i);
if(Character.isDigit(a))
{
int b=Integer.parseInt(String.valueOf(a)); sum=sum+b;
}
 


}
}
MAIN:
 
}
return sum;
 

import java.util.*;
public class Main {

public static void main(String[] args) {
// TODO Auto-generated method stub Scanner s=new Scanner(System.in);
String s1=s.next(); System.out.println(UserMainCode.getDigits(s1)); s.close();
}

}

	Password
USERMAINCODE:
public class UserMainCode {
public static boolean validatePassword(String s1)
{
boolean b=false; if(s1.length()>=8) b=true; if(b=true)
{
if(s1.matches(".*[0-9]{1,}.*")&&s1.matches(".*[a-zA-Z]{1,}.*")&&s1.matches(".*[@#%]{1,}.*"))
{
b=true;
}
else
b=false;
}
return b;
}
}
MAIN:
import java.util.*;
public class Main {
public static void main(String [] args)
{
Scanner s=new Scanner(System.in);
 String s1=s.nextLine();
boolean b=(UserMainCode.validatePassword(s1));
if(b==true)
{
System.out.println("Valid");
}
else System.out.println("Invalid"); s.close();
}
}
	Employee Bonus
USERMAINCODE:
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.ArrayList;
import java.util.Date; import java.util.Iterator;
import java.util.LinkedHashMap; import java.util.TreeMap;
class UserMainCode {
public static TreeMap<Integer,Integer> calculateRevisedSalary(LinkedHashMap<Integer,String>a1,LinkedHashMap<Integer,Integer>a2) throws ParseException
{TreeMap<Integer,Integer>ans=new TreeMap<Integer,Integer>(); ArrayList<String>al=new ArrayList<String>();
Iterator <Integer>it=a1.keySet().iterator(); while(it.hasNext())
{int s=it.next(); String s1=a1.get(s);
SimpleDateFormat sdf=new SimpleDateFormat("dd-MM-yyyy"); sdf.setLenient(false);
try{
 Date d=new Date(); Date d1=new Date(); String a=s1;
String b="01-09-2014";
d=sdf.parse(a); d1=sdf.parse(b); long t=d.getTime();
long t1=d1.getTime(); long t3=t1-t;
long l1=(24 * 60 * 60 * 1000); long l=l1*365;
long res=t3/l;
//System.out.println("Result="+res); if(res>=25 && res<=30)
{
float bonus=(float)((0.2*a2.get(s))+a2.get(s)); int r=(int)bonus;
ans.put(s,r );
}else if(res>30 && res<=60)
{
float bonus=(float)((0.3*a2.get(s))+a2.get(s)); int r=(int)bonus;
ans.put(s,r );
}
else if(a2.get(s)<5000)
{
ans.put(s, -100);
}
else if(res<25 ||res>60)
{
ans.put(s, -200);
}
}
catch (Exception e) { e.printStackTrace();
}
}
return ans;
}
}

MAIN:

import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.ArrayList;
import java.util.Date; import java.util.Iterator;
import java.util.LinkedHashMap; import java.util.Scanner;
import java.util.TreeMap; public class Main
{
public static void main(String args[]) throws ParseException{ Scanner sc=new Scanner(System.in);
int n=sc.nextInt();
LinkedHashMap<Integer,String>a1=new LinkedHashMap<Integer,String>(); LinkedHashMap<Integer,Integer>a2=new LinkedHashMap<Integer,Integer>(); TreeMap<Integer,Integer>ans=new TreeMap<Integer, Integer>();
 
for(int i=0;i<n;i++)
{int id=sc.nextInt(); a1.put(id,sc.next()); int salary=sc.nextInt(); a2.put(id,salary);
}
ans=UserMainCode.calculateRevisedSalary(a1,a2); Iterator <Integer>it=ans.keySet().iterator(); while(it.hasNext())
{
int a=it.next(); int b=ans.get(a);
System.out.println(a); System.out.println(b);
}
}
}

Grade Calculator REFER 53 FROM LEVEL2
USERMAINCODE:

import java.util.Iterator; import java.util.HashMap; import java.util.TreeMap; public class UserMainCode
{
public static TreeMap<Integer,String>calculateGrade(HashMap<Integer,Integer>hm)
{
TreeMap<Integer,String>tm=new TreeMap<Integer,String>(); Iterator<Integer>  it=hm.keySet().iterator(); while(it.hasNext())
{
int id=it.next();
int mark=hm.get(id); if(mark>=80) tm.put(id,"GOLD");
else if(mark<80 && mark>=60) tm.put(id,"SILVER");
else if(mark<60 && mark>=45) tm.put(id,"BRONZE");
else tm.put(id,"FAIL");
}
return tm;
}}

MAIN:

import java.util.HashMap; import java.util.Iterator; import java.util.HashMap; import java.util.TreeMap; import java.util.Scanner; public class Main {
public static void main(String []args){ Scanner sc=new Scanner(System.in);
 
int s=sc.nextInt();
HashMap<Integer,Integer>hm=new HashMap<Integer,Integer>(); for(int i=0;i<s;i++)
{
hm.put(sc.nextInt(),sc.nextInt());
}
TreeMap<Integer,String>tm=new TreeMap<Integer,String>(); tm=UserMainCode.calculateGrade(hm);
Iterator<Integer> it=tm.keySet().iterator(); for(int i=0;i<s;i++)
{
int n=it.next(); String fac=tm.get(n);
System.out.println(n); System.out.println(fac);
}
}
}
	Digits - II
MAIN:

import java.util.Scanner; public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in);
 int a=s.nextInt();
int sum=UserMainCode.getDigitSum(a); System.out.println(sum);
}
}
USERMAINCODE:
public class UserMainCode
{
public static int getDigitSum(int n)
{
int sum = 0 ; int n1=n; while(n>10)
{
int a = 0 ; sum = 0; while(n!=0)
{
a = n%10;
sum+=a; n=n/10;
}
n=sum;
}
 return sum;
}
}
	Anagrams
MAIN:
import java.util.*;
public class Main {
public static void main(String[] args){
Scanner s=new Scanner(System.in);
String s1=s.nextLine();
String s2=s.nextLine();
 System.out.println(UserMainCode.checkAnagram(s1,s2));
}
}
USERMAINCODE:
import java.util.*;
import java.text.*;
public class UserMainCode {
public static boolean checkAnagram(String s1,String s2)
{
boolean b=false;
String aj1 =s1.toLowerCase();	//ANAGRAMS String aj2=s2.toLowerCase();
ArrayList<Character> a1 = new ArrayList<Character>(); ArrayList<Character> a2	= new ArrayList<Character>(); for(int i=0;i<aj1.length();i++)
{
char c=aj1.charAt(i);
if(c!=' ')
{
 a1.add(c);
}
}
for(int j=0;j<aj2.length();j++)
{
char c=aj2.charAt(j);
if(c!=' ')
{
a2.add(c);
}
}
if(a1.size()==a2.size())
{
if(a1.containsAll(a2))
{
b= true;
}
}
return b;
}
}
	Shift Left
 MAIN:
import java.util.Scanner; public class Main {
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in); int size=sc.nextInt();
int[]m=new int[size]; int[]n=new int[size]; for(int i=0;i<size;i++)
{
 n[i]=sc.nextInt();
}
m=UserMainCode.shiftLeft(n); for(int i=0;i<size;i++)
{
System.out.println(m[i]);
}
}
}
USERMAINCODE:
public class UserMainCode {
public static int[] shiftLeft(int n[])
{
int j=0;
int[]m=new int[n.length]; for(int i=0;i<n.length;i++)
{
if(n[i]!=5)
{
m[j]=n[i]; j++;
}
}
return m;
 }
}
	Word Count
MAin:
import java.util.Scanner; public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); int n=s.nextInt();
String a[]=new String[n]; for(int i=0;i<n;i++)
{
 a[i]=s.next();
}
System.out.println(UserMainCode.sumOfDigits(a));
}
}
USERMAINCODE:
public class UserMainCode {
public static int sumOfDigits(String[] s1)
{
int sum = 0;
for(int i=0;i<s1.length;i++)
{
String s = s1[i];
for(int j = 0;j<s.length();j++)
{
Character c = s.charAt(j); if(Character.isDigit(c))
{
sum+=Integer.parseInt(s.valueOf(c));
}
}
}
return sum;
}
}
	Prefix Finder
MAIN:
import java.util.Scanner; public class Main {
public static void main(String[] args)
{
Scanner sc = new Scanner(System.in); int n=Integer.parseInt(sc.nextLine()); String s[]=new String[n];
for(int i=0;i<n;i++) s[i]=sc.nextLine();
System.out.println(UserMainCode.findPrefix(s));
}
}
USERMAINCODE:
import java.util.ArrayList; import java.util.Iterator;
import java.util.LinkedHashSet; public class UserMainCode
{
public static int findPrefix (String s[]) { LinkedHashSet<String>l1=new LinkedHashSet<String>(); ArrayList<String>a1=new ArrayList<String>();
int c=0;
for(int i=0;i<s.length;i++) l1.add(s[i]);
Iterator<String> it=l1.iterator(); while(it.hasNext())
{
a1.add(it.next());
}
for(int i=0;i<a1.size();i++)
{
String s2=a1.get(i);
for(int j=0;j<a1.size();j++)
{
String s3=a1.get(j); if(i!=j&&s3.length()>s2.length())
{
String s4=s3.substring(0,s2.length()); if(s2.equals(s4))
c++;
 }
}
}
return c;
}
}

	Commons
MAIN:
import java.util.Scanner;
public class Main {
public static void main(String[] args) { Scanner sc = new Scanner(System.in);
int n1 = sc.nextInt(); String[] s1 = new String[n1]; for (int i = 0; i < n1; i++) { s1[i] = sc.next();
 }
int n2 = sc.nextInt(); String[] s2 = new String[n2]; for (int i = 0; i < n2; i++) { s2[i] = sc.next();
}

System.out.println(UserMainCode.countCommonStrings(s1,s2));
}
}
USERMAINCODE:
import java.util.ArrayList;
public class UserMainCode {
public static int countCommonStrings(String[] s1,String[] s2)
{
int count=0;
ArrayList<String> al = new ArrayList<String>();
for (int i = 0; i < s1.length; i++) { for (int j = 0; j < s2.length; j++) { if(s1[i].equals(s2[j])){
if(!al.contains(s1[i])){
count++; al.add(s1[i]);
}
}
}
}
return count;
}
}
	Sequence Sum
MAIN:
import java.util.Scanner; public class Main {
public static void main(String[] args)
{
Scanner s=new Scanner(System.in); int n=s.nextInt();
System.out.println(UserMainCode.getFibonacciSum(n));
}
}
USERMAINCODE:
import java.util.ArrayList;
import java.util.Scanner; public class UserMainCode {
public static int getFibonacciSum(int n){ int a=0,b=1,c=0,d=1;
for(int i=3;i<=n;i++){ c=a+b;
a=b; b=c;
 d=d+c;
}
return d;
}
}
E-Mail Validation
 MAIN:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s=new Scanner(System.in);
String ip; ip=s.next();
boolean b=UserMainCode.ValidateEmail(ip);
if(b==true)
System.out.println("TRUE");
else
System.out.println("FALSE");
}}
USERMAINCODE:
import java.util.StringTokenizer;
public class UserMainCode {
public static boolean ValidateEmail(String ip) {
int i=0;
boolean b=false;
StringTokenizer t=new StringTokenizer(ip,"@"); String s1=t.nextToken();
String s2=t.nextToken();
StringTokenizer t1=new StringTokenizer(s2,"."); String s3=t1.nextToken();
String s4=t1.nextToken(); if(ip.contains("@") && ip.contains(".")) i++;
if(i==1) if(s3.length()==5) if(s1.length()>=3) if(s4.equals("com")) b=true;
return b;
}
}
	Symmetric Difference
MAIN:
import java.util.*;
public class Main
{
public static void main(String[] args)
{
int n,m;
Scanner sin = new Scanner(System.in);
n = sin.nextInt(); int[] a1 = new int[n]; for(int i=0;i<n;i++)
{
a1[i] = sin.nextInt();
}
m = sin.nextInt(); int[] a2 = new int[m]; for(int i=0;i<m;i++)
{
a2[i] = sin.nextInt();
}
int[] result = UserMainCode.getSymmetricDifference (a1,a2); for(int i=0;i<result.length;i++) System.out.println(result[i]);
}
}
USERMAINCODE:
import java.util.*;
public class UserMainCode
{
public static int[] getSymmetricDifference (int[] a1,int[] a2)
{
 
//int[] a1 = new int[]{11,5,14,26,3};

//int[] a2 = new int[]{5,3,1};
int[] union,inter,result;
int count=0;
int max = a1.length+a2.length;
ArrayList<Integer> temp = new ArrayList<Integer>(max);

/*union*/
for(int i=0;i<a1.length;i++)
{
if(!temp.contains(a1[i]))
{
++count; temp.add(a1[i]);
}
}
for(int i=0;i<a2.length;i++)
{
if(!temp.contains(a2[i]))
{
++count; temp.add(a2[i]);
}
}
union = new int[count]; for(int i=0;i<count;i++)
 {
union[i] = (int)temp.get(i);
}
Arrays.sort(union);
/*intersection*/
temp = new ArrayList<Integer>(max); count =0;
Arrays.sort(a2);
for(int i=0;i<a1.length;i++)
{
if(Arrays.binarySearch(a2,a1[i]) >= 0)
{
++count; temp.add(a1[i]);
}
}
inter = new int[count]; for(int i=0;i<count;i++)
{
inter[i] = (int)temp.get(i);
}
Arrays.sort(inter);
/*difference */
temp = new ArrayList<Integer>(max); count =0;
 Arrays.sort(inter);
for(int i=0;i<union.length;i++)
{
if(Arrays.binarySearch(inter,union[i]) < 0)
{
++count; temp.add(union[i]);
}
}
result = new int[count]; for(int i=0;i<count;i++)
{
result[i] = (int)temp.get(i);
}
Arrays.sort(result);

//System.out.println("resultant array : \n "+Arrays.toString(result));
return result;
}
}
	Day of Week
 MAIN:
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Scanner;
public class Main {
public static void main(String[] args) throws ParseException { Scanner sc=new Scanner(System.in);
 String s1=sc.nextLine(); System.out.println(UserMainCode.getDayofWeek(s1));
}
}
USERMAINCODE:
import java.text.SimpleDateFormat; import java.text.ParseException; import java.util.Date;
public class UserMainCode {
public static String getDayofWeek(String s1) throws ParseException
{
SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); SimpleDateFormat sdf1=new SimpleDateFormat("EEEEE"); Date d=sdf.parse(s1);
String s=sdf1.format(d);
return s.toLowerCase();
}
}
 	Add Time
MAIN:
import java.util.*;
import java.io.IOException;
import java.text.*;
public class Main {
public static void main(String[] args) throws IOException, ParseException { Scanner s = new Scanner(System.in);
String s1=s.next(); String s2=s.next();
System.out.println(UserMainCode.addTime(s1,s2));
}
}
USERMAINCODE:
import java.util.*;
import java.io.IOException;
import java.text.*;
 public class UserMainCode {
public static String addTime(String s1,String s2) throws IOException, ParseException{
SimpleDateFormat sdf=new SimpleDateFormat("HH:mm:ss"); sdf.setTimeZone(TimeZone.getTimeZone("UTC")); sdf.setTimeZone(TimeZone.getTimeZone("s1")); sdf.setTimeZone(TimeZone.getTimeZone("s2"));
Date d1=sdf.parse(s1); Date d2=sdf.parse(s2);
long add=d1.getTime()+d2.getTime(); String s=sdf.format(add);
Calendar cal=Calendar.getInstance(); cal.setTime(sdf.parse(s));
int FindDay=cal.get(Calendar.DAY_OF_MONTH);
if(FindDay>1) FindDay=FindDay-1; String op=FindDay+":"+s; return op;
}
}
	ISBN Validation
 MAIN:
import java.util.*;
public class Main {
public static void main(String[] args) { Scanner s = new Scanner(System.in);
String ip=s.next(); System.out.println(UserMainCode.ISBNnumber(ip));
}
}
USERMAINCODE:
import java.util.*;
import java.text.*;
public class UserMainCode {
public static String ISBNnumber(String ip) {
 String b="FALSE";
int sum=0;
for(int i=0,j=ip.length();i<ip.length();i++,j--){ String s=String.valueOf(ip.charAt(i));
int n=Integer.parseInt(s); sum+=(n*j); }
//System.out.println(sum);
if(sum%11==0) b="TRUE";
return b;
}
}
	Date Format
MAIN:
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.*;
public class Main {
public static void main(String[] args) throws ParseException { Scanner s = new Scanner(System.in);
String s1=s.next(); String s2=s.next();
System.out.println(UserMainCode.findOldDate(s1,s2));
}
}
 USERMAINCODE:
import java.text.ParseException; import java.text.SimpleDateFormat; import java.util.Calendar;
import java.util.Date;
public class UserMainCode {
public static String findOldDate(String s1,String s2) throws ParseException
{
SimpleDateFormat sdf=new SimpleDateFormat("dd/MM/yyyy"); SimpleDateFormat sdf1=new SimpleDateFormat("MM-dd-yyyy");
Date d1=sdf.parse(s1);
Date d2=sdf.parse(s2);
Calendar cal=Calendar.getInstance(); cal.setTime(d1);
long y=cal.getTimeInMillis(); cal.setTime(d2);
long y1=cal.getTimeInMillis(); String s3=sdf1.format(d1); String s4=sdf1.format(d2); if(y<y1)
return s3;
 else return s4;
}
}
	Interest Calculation
MAIN
import java.util.HashMap; import java.util.Iterator; import java.util.Scanner; import java.util.TreeMap; public class Main {
public static void main(String []args){ Scanner sc=new Scanner(System.in);
int s=Integer.parseInt(sc.nextLine()); HashMap<String,String>hm=new HashMap<String,String>(); HashMap<String,Integer>hm1=new HashMap<String,Integer>(); for(int i=0;i<s;i++)
{
String id=sc.nextLine(); hm.put(id, sc.nextLine());
hm1.put(id,Integer.parseInt(sc.nextLine()));
}
TreeMap<String,Integer>tm=new TreeMap<String,Integer>(); tm=UserMainCode.calculateInterestRate(hm,hm1); Iterator<String> it=tm.keySet().iterator(); while(it.hasNext())
{
String n=it.next();
int fac=tm.get(n);
 System.out.println(n+":"+fac);
}
}
}
USERMAINCODE
import java.text.DecimalFormat;
import java.text.SimpleDateFormat;
import java.util.Date; import java.util.HashMap; import java.util.Iterator; import java.util.HashMap;
import java.util.TreeMap;
public class UserMainCode
{
public static TreeMap<String,Integer> calculateInterestRate (HashMap<String,String>hm,HashMap<String,Integer>hm1)
{
int year=0,amount=0;
double dis=0;
String now="01/01/2015";
TreeMap<String,Integer>tm=new TreeMap<String,Integer>(); Iterator<String> it=hm.keySet().iterator();
 while(it.hasNext())
{
String id=it.next(); String dor=hm.get(id); amount=hm1.get(id);
SimpleDateFormat sdf=new SimpleDateFormat("dd-MM-yyyy"); SimpleDateFormat sdf1=new SimpleDateFormat("dd/MM/yyyy"); try
{
Date d=sdf.parse(dor); Date d1=sdf1.parse(now); sdf.setLenient(false); int y=d.getYear();
int y1=d1.getYear();
int m=d.getMonth();
int m1=d1.getMonth();
int day=d.getDay();
int day1=d1.getDay();
year=y1-y; if(m>m1) year--;
else if(m==m1)
{if(day<day1) year--;
}
 if(year>=60) dis=0.1*amount+amount;
else if(year<60 && year>=30 ) dis=0.07*amount+amount;
else dis=0.04*amount+amount; tm.put(id,(int)dis);
}
catch(Exception e)
{
e.printStackTrace();
}
}
return tm;
}
}
Discount Rate Calculation
MAIN:
import java.util.HashMap; import java.util.Iterator; import java.util.TreeMap; import java.util.Scanner; public class Main{
public static void main(String []args){ Scanner sc=new Scanner(System.in);
int s=Integer.parseInt(sc.nextLine()); HashMap<String,String>hm=new HashMap<String,String>(); HashMap<String,Integer>hm1=new HashMap<String,Integer>(); for(int i=0;i<s;i++)
 {
String id=sc.nextLine(); hm.put(id, sc.nextLine());
hm1.put(id,Integer.parseInt(sc.nextLine()));
}
TreeMap<String,Integer>tm=new TreeMap<String,Integer>(); tm=UserMainCode.calculateDiscount(hm,hm1); Iterator<String> it=tm.keySet().iterator(); while(it.hasNext())
{
String n=it.next();
int fac=tm.get(n); System.out.println(n+":"+fac);
}
}
}
USERMAINCODE
import java.text.SimpleDateFormat;
import java.util.Date; import java.util.HashMap; import java.util.*; public class UserMainCode
{
public static TreeMap<String,Integer> calculateDiscount (HashMap<String,String>hm,HashMap<String,Integer>hm1)
 {
int amount=0;
double dis=0;
String now="01/01/2015";
TreeMap<String,Integer>tm=new TreeMap<String,Integer>(); Iterator<String> it=hm.keySet().iterator(); while(it.hasNext())
{
String id=it.next(); String dor=hm.get(id); amount=hm1.get(id);
SimpleDateFormat sdf=new SimpleDateFormat("dd-MM-yyyy"); sdf.setLenient(false);
try{
Date d=new Date(); Date d1=new Date(); String a=dor;
String b="01-01-2014";
d=sdf.parse(a); d1=sdf.parse(b);  long t=d.getTime(); long t1=d1.getTime(); long t3=t1-t;
long l1=(24 * 60 * 60 * 1000);
long l=l1*365;
 long year1=t3/l;
//System.out.println("Result="+year1); if(year1>=5 && amount>=20000) dis=0.2*amount;
else if(year1<5 && amount>=20000) dis=0.1*amount;
else if(year1>=5 && amount<20000) dis=0.15*amount;
else dis=0.05*amount; tm.put(id,(int)dis);
}
catch(Exception e)
{
e.printStackTrace();
}
}
return tm;
}} 


