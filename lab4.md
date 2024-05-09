# Lab Report 3

> Part 1, Bugs:

A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown):

```
@Test
      public void testMergeWithFailure() {
          List<String> list1 = Arrays.asList("a", "c");
          List<String> list2 = Arrays.asList("b", "d", "e", "f");
          List<String> expected = Arrays.asList("a", "b", "c", "d", "e", "f");
          List<String> result = ListExamples.merge(list1, list2);
          assertEquals("Should merge both lists into a sorted order", expected, result);
      }
```

An input that doesn't induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown).

```
@Test
      public void testMergeWithoutFailure() {
          List<String> list1 = Arrays.asList("a", "c", "e");
          List<String> list2 = Arrays.asList("b", "d");
          List<String> expected = Arrays.asList("a", "b", "c", "d", "e");
          List<String> result = ListExamples.merge(list1, list2);
          assertEquals("Should merge both lists into a sorted order", expected, result);
      }
```

The symptom, as the output of running the two tests above (provide it as a screenshot -- one test should pass, one test should fail).

![Image](symptom.png)

The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown).

Before:
```
while(index2 < list2.size()) {
  result.add(list2.get(index2));
  index1 += 1;
}
return result;
```
After:
```
while(index2 < list2.size()) {
  result.add(list2.get(index2));
  index2 += 1;
}
return result;
```

Briefly describe (2-3 sentences) why the fix addresses the issue.
***
Changing the incriment from `index1` to `index2` ensures the loop is able to reach the elements in `list2`. This change ensures the loop does not go into an infinite loop, properly advancing through `list2`.

> Part 2, Researching Commands:

