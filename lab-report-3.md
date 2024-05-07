Part 1
1. Buggy Program
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
Failure-inducing Input
```
@Test
  public void addedTest1() {
    int[] input2 = { 5, 9, 3, 2, 6 };
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{ 6, 2, 3, 9, 5 }, input2);
  }
```
2. Non-failure-inducing Input
```
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
3. ![lab3](https://github.com/antspham/cse-15l-lab-report/assets/165956921/d8b577ea-46c1-4a0f-a05b-ba452acb9e03)
4. Before
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
After
```
static void reverseInPlace(int[] arr) {
   int placeholder = 0;
   for(int i = 0; i < arr.length/2; i += 1) {
     placeholder = arr[i];
     arr[i] = arr[arr.length - i - 1];
     arr[arr.length - i - 1] = placeholder;
   }
 }
```
5. The fix addresses the issue because the old code only changes the first half of the array overriding the first half of the array and not storing it to change the second half effectively which the new code does.

Part 2
Option -c displays the number of lines within the file that contain the string "he"
```
Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -c "he" chapter-1.txt
333

Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -c "he" chapter-2.txt
614
```
Option -i ignores case for matching
```
Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -i "HUNDRED" chapter-1.txt
    Washington Dulles: American 77. Hundreds of miles southwest of Boston, at Dulles International Airport in the Virginia suburbs of Washington, D.C., five more men were preparing to take their early morning flight. At 7:15, a pair of them, Khalid al Mihdhar and Majed Moqed, checked in at the American Airlines ticket counter for Flight 77, bound for Los Angeles. Within the next 20 minutes, they would be followed by Hani Hanjour and two brothers, Nawaf al Hazmi and Salem al Hazmi.

Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -i "HUNDRED" chapter-2.txt
                camps, but no more than a few hundred seem to have become al Qaeda members. From the
```
Option -n displays the line and line number where it contains the string "hundred", ignoring case from -i
```
Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -in "hundred" chapter-1.txt
38:    Washington Dulles: American 77. Hundreds of miles southwest of Boston, at Dulles International Airport in the Virginia suburbs of Washington, D.C., five more men were preparing to take their early morning flight. At 7:15, a pair of them, Khalid al Mihdhar and Majed Moqed, checked in at the American Airlines ticket counter for Flight 77, bound for Los Angeles. Within the next 20 minutes, they would be followed by Hani Hanjour and two brothers, Nawaf al Hazmi and Salem al Hazmi.

Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -in "hundred" chapter-2.txt
805:                camps, but no more than a few hundred seem to have become al Qaeda members. From the
```
Option -w looks for the exact string given within the file, so "hundreds" will only look for strings that are exactly "hundreds" and "hundred" would not satisfy this condition.
```
Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -iw "hundreds" chapter-1.txt
    Washington Dulles: American 77. Hundreds of miles southwest of Boston, at Dulles International Airport in the Virginia suburbs of Washington, D.C., five more men were preparing to take their early morning flight. At 7:15, a pair of them, Khalid al Mihdhar and Majed Moqed, checked in at the American Airlines ticket counter for Flight 77, bound for Los Angeles. Within the next 20 minutes, they would be followed by Hani Hanjour and two brothers, Nawaf al Hazmi and Salem al Hazmi.

Anthony@DESKTOP-QGBKVOI MINGW64 ~/CSE 15L/docsearch/technical/911report (main)
$ grep -iw "hundred" chapter-2.txt
                camps, but no more than a few hundred seem to have become al Qaeda members. From the
```
