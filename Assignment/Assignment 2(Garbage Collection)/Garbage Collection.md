Java Garbage Collection:
    Garbage Collection is process of reclaiming the runtime unused memory automatically. In other words, it is a way to destroy the unused objects.

    To do so, we were using free() function in C language and delete() in C++. But, in java it is performed automatically. So, java provides better memory management.

Advantage of Garbage Collection
    1) It makes java memory efficient because garbage collector removes the unreferenced objects from heap memory.
    2) It is automatically done by the garbage collector(a part of JVM) so we don't need to make extra efforts.


Example:

public class TestGarbage1{  
    public void finalize()
    {
        System.out.println("object is garbage collected");
    }

    public static void main(String args[])
    {  
        TestGarbage1 s1=new TestGarbage1();  
        TestGarbage1 s2=new TestGarbage1();  
        s1=null;  
        s2=null;  
        System.gc();
    }  
}

finalize() method
    The finalize() method is invoked each time before the object is garbage collected. This method can be used to perform cleanup processing. This method is defined in Object class as:

    protected void finalize(){}  