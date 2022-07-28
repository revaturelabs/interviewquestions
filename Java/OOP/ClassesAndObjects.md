## Error Detection

1. Find the error in the following code?

``` java
public class Game {
	public static void main(String[] args) {
		Game g;
		g.playCricket();
		
		
	}
	void playCricket() {
		System.out.println("I am a Batsman");
	}

}

```

<details><summary>Show Answer</summary>

<b>Ans:</b> The above code creates a compile-time error, The object "g" is declared but not initialized, and It is not possible to use an object of a class without Initializing it.

</details>
