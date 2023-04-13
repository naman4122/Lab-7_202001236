# Lab-7_202001236

# Name: Naman Patel

# Section-A

**Equivalence Partitioning Test Cases:**

| **Tester Action and Input Data** | **Expected Outcome** |
| ---------------------------------|----------------------|
| Valid input: day=1, month=1, year=1900 | Invalid date |
| Valid input: day=31, month=12, year=2015 | Previous date |
| Invalid input: day=0, month=6, year=2000 | An error message |
| Invalid input: day=32, month=6, year=2000 | An error message |
| Invalid input: day=29, month=2, year=2001	 | An error message |

**Boundary Value Analysis Test Cases:**

| **Tester Action and Input Data** | **Expected Outcome** |
| ---------------------------------|----------------------|
| Valid input: day=1, month=1, year=1900 | Invalid date |
| Valid input: day=31, month=12, year=2015 | Previous date |
| Invalid input: day=0, month=6, year=2000 | An error message |
| Invalid input: day=32, month=6, year=2000 | An error message |
| Invalid input: day=29, month=2, year=2000 | An error message |
| Valid input: day=1, month=6, year=2000 | Previous date |
| Valid input: day=31, month=5, year=2000 | Previous date |
| Valid input: day=15, month=6, year=2000 | Previous date |
| Invalid input: day=31, month=4, year=2000 | An error message |

**Problem -A**

          import org.junit.Test;
          import static org.junit.Assert.*;

          public class LinearSearchTest {

            @Test
            public void testExistingValue() {
              int[] arr = {1, 2, 3, 4, 5};
              int index = linearSearch(3, arr);
              assertEquals(2, index);
            }

            @Test
            public void testNonExistingValue() {
              int[] arr = {1, 2, 3, 4, 5};
              int index = linearSearch(6, arr);
              assertEquals(-1, index);
            }

            @Test
            public void testFirstElement() {
              int[] arr = {1, 2, 3, 4, 5};
              int index = linearSearch(1, arr);
              assertEquals(0, index);
            }

            @Test
            public void testLastElement() {
              int[] arr = {1, 2, 3, 4, 5};
              int index = linearSearch(5, arr);
              assertEquals(4, index);
            }

            @Test
            public void testEmptyArray() {
              int[] arr = {};
              int index = linearSearch(1, arr);
              assertEquals(-1, index);
            }

            @Test
            public void testNullArray() {
              int[] arr = null;
              int index = linearSearch(1, arr);
              assertEquals(-1, index);
            }
          }
