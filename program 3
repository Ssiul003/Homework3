/* The agecaluclator program is suppose to calculate an age when given the date
in the form like 6 7 2003. I had trouble using useDelimiter and had it for "/"
but it was giving me inputmismatchexception. I also remember how the scanner
could include the titles like month,day,year but I forgot how the HW2 program
was shown during class. The program should run as long as there is a files.txt
called dates.txt and  the date should be formatted like 6 8 2004 because
I couldnt find a way to get rid of the inputmismatchexceptiong error.

*/
package su22hw3;

import java.time.LocalDate;
import java.time.Period;
import java.util.Scanner;
import java.io.File;

public class Su22Hw3 {

    public static void main(String[] args) throws Exception {
        Scanner scanner = new Scanner(new File("dates.txt"));

        int month, day, year;
        while (scanner.hasNext()) {

            month = scanner.nextInt();
            day = scanner.nextInt();
            year = scanner.nextInt();

            System.out.printf("Your date of birth is %d/%d/%d.\n", month, day, year);
//The LocalDate is something I got from online and it finds the difference
//between the current date and date of birth.
            LocalDate dob = LocalDate.of(year, month, day);

            LocalDate curDate = LocalDate.now();

            Period period = Period.between(dob, curDate);

            System.out.printf("Your age is %d years.\n", period.getYears());
        }
    }
}
