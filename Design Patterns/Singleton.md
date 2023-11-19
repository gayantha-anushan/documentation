# Singleton Design Pattern

### Why?

if we want to use just one object instance but your class will call in different places then you can use singleton design pattern.
### Steps
1. Create class
2. Create class's instance property
3. Create getInstance Method
4. Make constructor as private
5. verify that instance and getinstance methods are static
### Example

**MyAction.cs**
```
class MyAction{
    private static MyAction? Instance = null;

    private MyAction(){
        //
    }

    public static getInstance(){
        if(Instance == null){
            Instance = new MyAction();
        }
        return Instance;
    }

    public void ShowMessage(){
        Console.Writeline("Show Messages Now!");
    }
}
```

**Program.cs**
```
MyAction action = MyAction.getInstance();
action.ShowMessage();
```