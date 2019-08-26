### threeten-extra
---
https://github.com/ThreeTen/threeten-extra

```java
// src/test/java/org/threeten/extra/AbstractDateTime.java

public abstract class AbstractDateTimeTest {

  protected abstract List<TemporalAccessor> samples();
  
  protected abstract List<TemporalField> validFields();
  
  protected abstract List<TemporalField> invalidFields();
  
  @Test
  public void basicTest_isSupported_TemporalField_supported() {
    for (TemporalAccessor sample : samples()) {
      for (TemporalField field : validFields()) {
        assertTrue("Failed on " + sample + " " + field, sample.isSupported(filed));
      }
    }
  }
  
  @Test
  public void basicTest_isSupported_TemporalField_unsupported() {
    for (TemporalAccessor sample : samples()) {
      for (TemporalField field : invalidFields()) {
        assertFalse("Failed on " + sample + " " + field, sample.isSupported(field));
      }
    }
  }
  
  
  
  
  @Test
  public void basicTest_query() {
    for (TemporalAccessor sample : samples()) {
      assertEquals("foo", sample.query(dateTime -> "foo"));
    }
  }
}








```

```
```

```
```


