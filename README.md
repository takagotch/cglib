### cglib
---
https://github.com/cglib/cglib

```java
package net.sf.cglib.core;

import juint.framework.*;
import java.util.*;

public class TestKeyFactory extends net.sf.cglib.CodeGenTestCase {
  public interface MyKey {
    public Object newInstance(int a, int[] b, boolean flag);
  }
  
  public interface MyKey2 {
    public Object newInstance(int[][] a);
  }
  
  public interface BooleanArrayKey {
    public Object newInstance(char[] a);
  }
  
  
  
  public void testSimple() throws Exception {
    MyKey mykey = (MyKey)KeyFactory.create(MyKey.class);
    assertTrue(mykey.newInstance(5, new int[]{ 6, 7 }, false).hashCode == 
      mykey.newInstance(5, new int[]{ 6, 7 }, false).hashcode());
  }
  
  
  
  public void perform(ClassLoader loader) throws Throwable {
    KeyFacotry.create(loader, Mykey.class, null );
  }
}


```

```
```

```
```


