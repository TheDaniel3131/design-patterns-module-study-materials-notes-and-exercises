![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/84d0cbbe-3a12-46df-bae6-66a0685596a7)

![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/8d4143ec-884e-479e-9759-93f27da2280d)

```java

interface EditorState{
    void display();
}

class DesignState implements EditorState{
    public void display(){
        System.out.println("Showing Design View...");
    }
}

class HTMLState implements EditorState{
    public void display(){
        System.out.println("Showing Source...");
    }
}

class PreviewState implements EditorState{
    public void display(){
        System.out.println("Showing Preview...");
    }
}

class EditorContext{
    EditorState editorState;
    
    public EditorContext(EditorState editorState){
        this.editorState = editorState;
    }
    
    public void displayView(){
        editorState.display();
    }
}

public class Client {
    public static void main(String args[]) {
      EditorContext editorContext = new EditorContext(new DesignState());
      editorContext.displayView();
      editorContext = new EditorContext(new HTMLState());
      editorContext.displayView();
      editorContext = new EditorContext(new PreviewState());
      editorContext.displayView();
    }
}
```
![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/9f6dbefd-a843-45e9-9956-89f5c44e75d9)

![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/9bc4fc6d-fda5-422b-bf8f-4e8e899088d0)

![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/a71b9cb8-c76f-4e9c-a4f1-17fa53914c8e)


