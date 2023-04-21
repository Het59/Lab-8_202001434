# IT-314 SOFTWARE ENGINEERING LAB - 8
### Student_ID: 202001434 
### Name: Het Patel
---

#### 3.Boa.java file

```
package Junit;


import static org.junit.Assert.*;


import org.junit.Before; import org.junit.Test;


public class BoaTest {

  private Boa jen; 
  private Boa ken;
  
  @Before
  public void setUp() throws Exception {
    jen = new Boa("Jennifer", 2, "grapes");
    ken = new Boa ("Kenneth", 3, "granola bars");
    
  }
  @Test
   public void testIsHealthy_1() { 
    boolean output = jen.isHealthy(); 
    assertEquals(output,false);
  }
  @Test
  public void testFitsInCage_1()
  { 
    boolean output = jen.fitsInCage(5); 
    assertEquals(output, true);
  }
} 
```

![image](https://user-images.githubusercontent.com/124347145/233607716-e12bdb1a-c41b-44fb-aa48-6ad720d3e9f1.png)

#### 4.Modify Setup method:
BoaTest.java file:
```
package Junit;

import static org.junit.Assert.*; 
import org.junit.Before;

import org.junit.Test; public class BoaTest {

  private Boa jen; 
  private Boa ken; 
  
  @Before
  public void setUp() throws Exception {
    jen = new Boa("Jennifer", 2, "grapes");
    ken = new Boa ("Kenneth", 3, "granola bars"); 
  }
}
```
![image](https://user-images.githubusercontent.com/124347145/233608469-6a400658-441b-4784-bfbf-08814a89f612.png)

#### 5.@Test stubs
* A. Testing for testIshealthy() function:
   * Code:
    ```
    @Test
    public void testIsHealthy() { 
      boolean output = jen.isHealthy(); 
      assertEquals(output,false);
    }
    ```
  I created two test case for testIshealthy function and test as below.mow we test using junit testing method.

  **1.testIshealthy1()**
  ![image](https://user-images.githubusercontent.com/124347145/233609232-6d07a23b-5095-4f0a-b047-6fcc9b47de1f.png)

  **2.testIshealthy2()**
  ![image](https://user-images.githubusercontent.com/124347145/233609405-8f9129b7-f5e6-40e7-91b7-e8cc10ad4ca6.png)

* B. Testing for
  * testFitsInCage() 
  Code:
    ```
    @Test
    public void testFitsInCage() { 
      boolean output = jen.fitsInCage(5); 
      assertEquals(output, true);
     }
    ```
  I created three test cases for function testFitsInCage()and test as below.mow we test using junit testing method.
  
  **1.testFitsInCage_1()**
  ![image](https://user-images.githubusercontent.com/124347145/233610062-b587db6e-515e-4e45-a08f-4448635d6233.png)
  
  **2.testFitsInCage_2()**
  ![image](https://user-images.githubusercontent.com/124347145/233610158-cc5ff4c8-3ee2-49e7-be67-63ad264f19b8.png)

  **3.testFitsCage_3()**
  ![image](https://user-images.githubusercontent.com/124347145/233610265-4301a88a-4f15-454e-94c5-ef6b523df47a.png)
  
#### 7. Add a new method to the Boa class, with this purpose and signature:
```
// produces the length of the Boa in inches 
public int lengthInInches(){
  // you need to write the body of this method
}
```
Adding new method:

**Testing for lengthInInches()**
I created the two test case for lengthininches() function and then using junit testing method.
code:

```
@Test
public void lengthInInches() {
  int output = jen.lengthInInches(); 
  assertEquals(output, 24);
}
```
**1.lengthInInches_1()**
![image](https://user-images.githubusercontent.com/124347145/233614512-bc801b1f-62f7-444a-8666-e5ac5b2215c5.png)

**2.lengthInInches_2()** 
![image](https://user-images.githubusercontent.com/124347145/233614582-57809c04-0c59-4a6b-9e11-ebdf0c45ad31.png)

The modified testFitsInCage() method tests the results of the fitsInCage() method when the cage length is less than, equal to, and greater than the length of the boa for both healthyBoa and unhealthyBoa objects.

Since the setUp() method initializes two different Boa objects, healthyBoa and unhealthyBoa, there is no need to write separate tests for "jen" and "ken". The tests should cover both objects as specified in the setUp() method.

