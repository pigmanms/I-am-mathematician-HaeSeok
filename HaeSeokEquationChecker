import java.util.*;

public class HaeSeokEquationChecker {
    public static void main(String[] args) {
        int zMax = 100; // Adjust the range of z as needed
        int xMilestone = 20;
        int yMilestone = 20;

        Set<Integer> seenZValues = new HashSet<>(); //tf how to use this s f

        for (int x = 0; x <= zMax; x++) {
            for (int y = 0; y <= zMax; y++) {
                int z = (int) Math.sqrt(x + y);

                if (z * z == x + y) {
                    if (seenZValues.contains(z)) {
                        System.out.printf("(%d, %d): z^2 = %d + %d, ToF: true, z = %d (appeared)%n", x, y, x, y, z);
                    } else {
                        System.out.printf("(%d, %d): z^2 = %d + %d, ToF: true, z = %d%n", x, y, x, y, z);
                        seenZValues.add(z);
                    }
                } else {
                    System.out.printf("(%d, %d): z^2 = %d + %d, ToF: false%n", x, y, x, y);
                }

                // Reset y and increase x when y reaches the milestone limit
                if (y == yMilestone) {
                    x++;
                    y = 0;
                    //here no longer available. // Increase the milestone limit for y only when x reaches its milestone
                }
            }

            // Reset x and increase y limit when x reaches the milestone limit
            if (x == xMilestone) {
                x = 0;
                xMilestone += 20; // Increase the milestone limit for x
                yMilestone += 20; // Increase the milestone limit for y when x reaches its milestone
            }
        }
    }
}
