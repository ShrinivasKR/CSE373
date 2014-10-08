package app;
import java.util.ArrayList;
import java.awt.image.BufferedImage;


public class ImageStack {
	private ArrayList<BufferedImage> edits;
	private boolean wasPop;
	
	//constructer method to create an ImageStack for use
	public ImageStack() {
		edits = new ArrayList<BufferedImage>();
		wasPop = false;
	}
	
	//enters the data item onto the stack and returns nothing
	public void push(BufferedImage entry) {
		edits.add(entry);
		wasPop = false;
	}
	
	//throws an exception if the stack is empty; otherwise returns the top element, removing it from the stack.
	public BufferedImage pop() throws Exception {
		try { 
			BufferedImage temp = edits.remove(edits.size() - 1);
			wasPop = true;
			return temp;
		} catch (Exception StackIsEmpty) {
			return null;
		}		
	}
	
	//throws an exception if the stack is empty; otherwise returns the top element of the stack. However, unlike pop, it does not change the contents of the stack.
	public BufferedImage peek() throws Exception {
		try {
			return edits.get(edits.size() - 1);
		} catch (Exception StackIsEmpty) { 
			return null;
		}
	}
	
	//returns true if there are no items in the stack; false otherwise.
	public boolean isEmpty() {
		return edits.isEmpty();
	}
	
	//makes the stack empty.
	public void clear() {
		edits.clear();
		wasPop = false;
	}
	
	
	//returns true if the last push, pop, or clear operation was a pop and false otherwise. If neither a push nor a pop nor a clear has yet been executed, then false is returned.
	public boolean popWasLast() {
		return wasPop; 
	}
	
	//returns the number elements currently in the stack.
	public int getSize() {
		return edits.size();
	}
	
}
