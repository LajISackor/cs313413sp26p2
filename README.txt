COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		No difference for correctness as both pass the same tests because both implement List.
		The difference is mainly performance

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			Removes the element at index 5 (the 6th element), because 5 is an int so it uses remove(int index).

		list.remove(Integer.valueOf(5)); // what does this one do?

			Removes the first occurrence of the value 5, because it calls remove(Object o).

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			i.remove() safely removes the current element while iterating. If you use list.remove(77) during iteration,
			it can cause a ConcurrentModificationException because the list is being modified outside the iterator.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.
	These are examples of SIZEs you might choose, you can choose others if you wish.

	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	listAccess - which type of List is better to use, and why?

		ArrayList is better for access because getting elements by index is fast (O(1)).
		While LinkedList is slower for access because it must move through nodes (O(n)).


	listAddRemove - which type of List is better to use, and why?

		LinkedList can be better for adding or removing in the middle if you already have an iterator at that position.
		While ArrayList must shift elements, which takes more time. However, for adding at the end, ArrayList is very fast.