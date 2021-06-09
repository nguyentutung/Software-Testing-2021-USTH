Ex3.5:
@Test
public void testSort()
{
names.add ("Laura");23
names.add ("Han");
names.add ("Alex");
names.add ("Ashley");
names.sort();
assertTrue ("Sort method", names.getFirst().equals ("Alex"));
}
Only the first element is checked in this assertion. Model RIRP: Reachability: If there is a problem with the initial element, it is reached at that moment. It hasn't come to that 
for the first element. Infection: Yes. Revealability: No, the test declaration will not reveal the flaw. Propagation: No, it's not true. Even if the entire list is sorted 
incorrectly, the major component can still be "Alex." The test condition would be satisfied and redressed, but the contaminated state would remain undetected.
