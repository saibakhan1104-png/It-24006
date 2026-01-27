package ict_22; 
 
public class SumClass { 
    public static double calculateSum() { 
        double sum = 0.0; 
        for (double i = 1.0; i >= 0.01; i=i-0.1) { 
            sum = sum+ i; 
        } 
        return Math.round(sum); 
    } 
}  
 
package ict_22; 
 
public class DivisorMultipleClass { 
    public static int gcd(int a, int b) { 
        while (b != 0) { 
            int temp = b; 
            b = a % b; 
            a = temp; 
        } 
        return a; 
    } 
 
    public static int lcm(int a, int b) { 
        return (a * b) / gcd(a, b); 
    } 
} 
 

  
package ict_22; 
 
public class NumberConversionClass { 
    public static String decimalToBinary(int decimal) { 
        return Integer.toBinaryString(decimal); 
    } 
 
    public static String decimalToOctal(int decimal) { 
        return Integer.toOctalString(decimal); 
    } 
 
    public static String decimalToHex(int decimal) { 
        return Integer.toHexString(decimal).toUpperCase(); 
    } 
 
    public static int binaryToDecimal(String binary) { 
        return Integer.parseInt(binary, 2); 
    } 
 
    public static int octalToDecimal(String octal) { 
        return Integer.parseInt(octal, 8); 
    } 
 
    public static int hexToDecimal(String hex) { 
        return Integer.parseInt(hex, 16); 
    } 
} 
  4) CustomPrintCLass:  
package ict_22; 
 
public class CustomPrintClass { 
    public static void pr(String msg) { 
        System.out.println(msg); 
    } 
              } 
 
         
package ict_22; 
 
public class MainClass { 
    public static void main(String[] args) { 
 
        CustomPrintClass.pr("===== PROGRAM STARTED ====="); 
        double sum = SumClass.calculateSum(); 
        CustomPrintClass.pr("Sum of 1 + 0.9 + ... + 0.1 = " + sum); 
        int a = 12, b = 18; 
        CustomPrintClass.pr("GCD of " + a + " and " + b + " = " + DivisorMultipleClass.gcd(a, 
b)); 
        CustomPrintClass.pr("LCM of " + a + " and " + b + " = " + DivisorMultipleClass.lcm(a, 
b)); 
        int dec = 25; 
        CustomPrintClass.pr("Decimal " + dec + " -> Binary = " + 
NumberConversionClass.decimalToBinary(dec)); 
        CustomPrintClass.pr("Decimal " + dec + " -> Octal = " + 
NumberConversionClass.decimalToOctal(dec)); 
        CustomPrintClass.pr("Decimal " + dec + " -> Hexadecimal = " + 
NumberConversionClass.decimalToHex(dec)); 
        CustomPrintClass.pr("Binary 11001 -> Decimal = " + 
NumberConversionClass.binaryToDecimal("11001")); 
        CustomPrintClass.pr("Octal 31 -> Decimal = " + 
NumberConversionClass.octalToDecimal("31")); 
        CustomPrintClass.pr("Hex 19 -> Decimal = " + 
NumberConversionClass.hexToDecimal("19")); 
 
        CustomPrintClass.pr("===== PROGRAM ENDED ====="); 
    } 
} 
