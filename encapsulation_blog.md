Encapsulation: a poorly encapsulated object can have its internal "data" modified
by public methods, whereas a well encapsulated object does not allow this.
Well encapsulated objects are necessary so that users cannot modify objects in
ways unwanted by a system. In the example below, we can create an instance of a
Person and easily change his or her name.

```
Class Person
  attr_accessor :first_name, :last_name

  def initialize(first_name, last_name)
    @first_name = first_name
    @last_name = last_name
  end

  def full_name
    first_name + " " + last_name
  end

end
```
To refactor this code to provide better encapsulation, we would simply have to
replace attr_accessor with attr_reader.
