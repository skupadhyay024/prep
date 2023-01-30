### Program
* Max and Min in an array
* Implement Stack using Array or ArrayList
* ``` package com.spa;

import java.util.ArrayList;
import java.util.List;

public class Sample {
	
	private static  final String COMMA = ",";


	public static void main(String[] args) {
		
		System.out.println(formatItemNumber("23-00-033-17,-19"));
		System.out.println(formatItemNumber("22-11-00-2, 22-00-007-01, 22-00-008-01"));
		System.out.println(formatItemNumber("21-53-14, 23-53-18, see INFO message"));
		System.out.println(formatItemNumber("play INFO game"));
		System.out.println(formatItemNumber("21-34-21, 12-34-21, PLAY"));
		System.out.println(formatItemNumber("21-32-32, -16, -41, 32-12-12, -15, go INFO chat"));		

	}
	
	public static List<String> formatItemNumber(String itemNumber) {
		String itemNumberWithoutOR = itemNumber.replaceAll("OR", COMMA);
	    String [] itemNumbers = itemNumberWithoutOR.replaceAll("\\s", "").split(COMMA);
	    List<String> finalItemNumberList = new ArrayList<String>();
	    String lastValidNumber = itemNumbers[0];
	    for(String item: itemNumbers) {
	    	if(item.contains("INFO")) {
	    		continue;
	    	}
	    	if(item.startsWith("-")) {
	    		finalItemNumberList.add(lastValidNumber + item);
	    		
	    	}else if (item.contains("-")) {
	    		lastValidNumber = item.substring(0,item.lastIndexOf("-"));
	    		finalItemNumberList.add(item);
	    	} else {
	    		finalItemNumberList.add(item);
	    	}
	    	
	    }
	    return finalItemNumberList;
}

	} ```
  
**[23-00-033-17, 23-00-033-19]  
[22-11-00-2, 22-00-007-01, 22-00-008-01]  
[21-53-14, 23-53-18]  
[]  
[21-34-21, 12-34-21, PLAY]  
[21-32-32, 21-32-16, 21-32-41, 32-12-12, 32-12-15]**
