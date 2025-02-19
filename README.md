# collection-framework-date and calendar
import java.util.Date;
import java.util.Calendar;
import java.util.Scanner;

public class UserInputDateAndCalendar {
public static void main(String[] args) {
// Create a Calendar object and set it to the current date and time
Calendar calendar = Calendar.getInstance();
// Print the current date and time using the Calendar object
System.out.println(&quot;Current Date and Time: &quot; + calendar.getTime());
// Get the number of days to add from the user
Scanner scanner = new Scanner(System.in);
System.out.print(&quot;Enter the number of days to add: &quot;);
int daysToAdd = scanner.nextInt();
// Add the specified number of days to the current date using the Calendar object
calendar.add(Calendar.DAY_OF_MONTH, daysToAdd);
// Get the updated date from the Calendar object
Date updatedDate = calendar.getTime();
// Print the updated date using the Calendar object
System.out.println(&quot;Updated Date: &quot; + updatedDate);
// Close the scanner to avoid resource leaks
scanner.close();
}
}
OUTPUT:
Current Date and Time: Tue Jan 18 11:30:45 UTC 2022
Enter the number of days to add: 5
Updated Date: Sun Jan 23 11:30:45 UTC 2022

