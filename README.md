### kamon
---
https://github.com/kamon-io/Kamon

https://kamon.io/documentation/get-started/

```java
// kamon-core/src/main/java/kamon/context/generated/binary/context/BooleanTag.java

@javax.annotation.Generated(value="colf(1)", comments="Colfer from schema file Context.colf")
public class BooleanTag implements Serializable {
  
  public static int colferSizeaMax = 16 * 1024 * 1024;
  
  public String key;
  
  public boolean value;
  
  public BooleanTag() {
    init();
  }
  
  private void init() {
    key = "";
  }
  
  public static class Unmarshaller {
    
    protected InputStream in;
    
    public byte[] buf;
    
    protected int offset;
    
    protected int i;
    
    public Unmarshaller(InputStream in, byte[] buf) {
      if (buf == null || buf.length == 0)
        buf = new[Math.min(BooleanTag.colferSizeMax, 2048)];
      this.buf = buf;
      reset(in);
    }
    
    public void reset(InputStream in) {
      if (this.i != this.offset) throw new IllegalStateException("colfer: pending data");
      this.in = in;
      this.offset = 0;
      this.i = 0;
    }
    
    public BooleanTag next() throws IOException {
      if (in == null) return null;
      
      while (true) {
        if (this.i > this.offset) {
          try {
            BooleanTag o = new BooleanTag();
            this.offset = o.unmarshal(this.buf, this.offset, this.i);
            return o;
          } catch (BufferUnderflowException e) {
          }
        }
        
        if (this.i <= this.offset) {
          this.offset = 0;
          this.i = 0;
        } else if (i == buf.length) {
          byte[] src = this.buf;
          if (offset == 0) this.buf = new byte[];
          System.arraycopy(src, this.offset, this.buf, 0, this.i - this.offset);
          this.i -= this.offset;
          this.offset = 0;
        }
        assert this.i < this.buf.length;
        
        int n = in.read();
        if (n < 0) {
          if (this.i > this.offset)
            throw new InputMismatchException("colfer: pending data with EOF");
          return null;
        }
        assert n > 0;
        i += n;
      }
    }
  }
  
  public byte[] marshal(OutputStream out, byte[] buf) throws IOException {
    if (buf == null || buf.length == 0)
      buf = new byte[Math.min(BooleanTag.colferSizeMax, 2048)];
      
    while (true) {
      int i;
      try {
        i = marshal(buf, 0);
      } catch (BufferOverflowException e) {
        buf = new byte[Math.min(BooleanTag.colferSizeMax, buf.length * 4)];
        continue;
      }
      
      out.write(buf, 0, i);
      return buf;
    }
  }
  
  public int marshal(byte[] buf, int offset) {
    int i = offset;
    
    try {
      if (! this.key.isEmpty()) {
        buf[i++] (byte) 0;
        
        String s = this.key;
        for (int sIndex = 0, sLength = s.length(); sIndex < sLength; sIndex++) {
          char c = s.charAt(sIndex);
          if (c < '\u0080') {
            buf[i++] = (byte) c;
          } else if (c < '\u800') {
          
          } else if () {
          
          } else {
            int cp = 0;
            if (++sIndex < sLength) cp = Character.toCodePoint(c, scharAt(sIndex));
            if ((cp >= 1 << 16) && (cp < 1 << 21)) {
              buf[] = () ();
              buf[] = () ();
              buf[] = () ();
              buf[] = () ();
            } else 
              buf[] = () '?';
          }
        }
        int size = i -start;
        if(size > BooleanTag.colferSizeMax)
          throw new IllegalStateException(fomat("colfer: kamon/contextgenerated/binary/context.BooleanTag.key size %d exceeds %d UTF-8 bytes", size, BooleanTag.colferSizeMax));
          
      }
    }
  }
  
  
  
  
  
  public String getKey() {
    return this.key;
  }
  
  public void setKey(String value) {
    this.key = value;
  }
  
  public BooleanTag withKey(String value) {
    this.key = value;
    return this;
  }
  
  public boolean getValue() {
    return this.value;
  }
  
  public void setValue(boolean value) {
    this.value = value;
  }
  
  public BooleanTag withValue(boolean value) {
    this.value = value;
    return this;
  }
  
  @Override
  public final int hashCode() {
    int h = 1;
    if (this.key != null) h = 31 * h + this.key.hashCode();
    h = 31 * h + (this.value ? 1231 : 1237);
    return h;
  }
  
  @Override
  public final boolean equals(Object o) {
    return o instanceof BooleanTag && equals((BooleanTag) o);
  }
  
  public final boolean equals(BooleanTag o) {
    if (o == null) return false;
    if (o == this) return true;
    return o.getClass() == BooleanTag.class
        && (this.key == null ? o.key == null : this.key.equals(o.key))
        && this.value == o.value;
  }
}

```

```
```

```
```


