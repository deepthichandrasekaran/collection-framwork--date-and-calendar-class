# collection-framwork--date-and-calendar-class
import java.util.HashMap;
import java.util.Hashtable;
import java.util.Map;
import java.util.Scanner;
public class SimpleUserInputMap {
public static void main(String[] args) {
// Create a HashMap and a Hashtable
Map&lt;String, Integer&gt; hashMap = new HashMap&lt;&gt;();
Map&lt;String, Integer&gt; hashtable = new Hashtable&lt;&gt;();

// Get key-value pairs from the user
Scanner scanner = new Scanner(System.in);
System.out.print(&quot;Enter key-value pairs (key1=value1 key2=value2 ...): &quot;);
String input = scanner.nextLine();
// Parse the input string and add key-value pairs to both maps
String[] keyValuePairs = input.split(&quot;\\s+&quot;);
for (String pair : keyValuePairs) {
String[] keyValue = pair.split(&quot;=&quot;);
if (keyValue.length == 2) {
String key = keyValue[0];
int value = Integer.parseInt(keyValue[1]);
hashMap.put(key, value);
hashtable.put(key, value);
}
}
// Print keys and values of both maps
System.out.println(&quot;HashMap: &quot; + hashMap);
System.out.println(&quot;Hashtable: &quot; + hashtable);
// Close the scanner to avoid resource leaks
scanner.close();
}
}
OUTPUT:
Enter key-value pairs (key1=value1 key2=value2 ...): name= Anu city=coimbatore
HashMap: {name=Anu, city=coimbatore}
Hashtable: {name=Anu, city=coimbatore}
