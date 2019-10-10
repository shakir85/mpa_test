# HashMap
Test if a map is a subset of another map or not

```java
public class MapSubset {
	
	public static void main(String[] args) {
		int count=0;
		Map<String, String> mp1 = new HashMap<>();
		Map<String, String> mp2 = new HashMap<>();
		mp1.put("1", "foo");
		mp1.put("2", "bar");
		mp1.put("3", "wow");
		
		mp2.put("1","foo");
		mp2.put("2", "bar");
		mp2.put("3", "zoo");
		
    //put all the keys in a set
		Set<String> s1 = mp1.keySet(); 
		Set<String> s2 = mp2.keySet();
		
    //Logic
		for(String i : s1)
			for(String j : s2)
				if(mp1.get(i).equals(mp2.get(j))) 
					System.out.println("Map 1 has: " +mp1.get(i) + " | Map 2 has: " + (mp2.get(j)));
					count++;
		System.out.println("match =" + count);
	}
}
```
