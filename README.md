# Checkpoint 04

> If you have not completed the survey yet,
please do so by the end of the day!

## Instructions

1. Fork this repo
2. Clone your fork
3. Fill in your answers by writing in the appropriate area, or placing an 'x' in
the square brackets (for multiple-choice questions).
4. Add/Commit/Push your changes to Github.
5. Open a pull request.

> **Note**: Only place your answer between backticks. Don't modify the backticks,
or the language specifier after them.

## Ruby Basics & Enumerables (meets Beauty and the Beast)

### Question 1

Define a method called `offer_rose`, which should take one argument named `person`.

When called the method should `puts` "Would you take this rose, `person`, in exchange for giving an old beggar woman shelter from the bitter cold?"

Demonstrate calling the method, passing in "young prince" as the argument.

Write your code here:
```ruby

def offer_rose person
  @person = person
  puts "Would you take this rose, #{@person}, in exchange for giving an old beggar woman shelter from the bitter cold?"
end

offer_rose "young prince"
```

### Question 2

Assume the following hash:

```ruby
town = {
  residents: ["Maurice", "Belle", "Gaston"],
  castle: {
    num_rooms: 47,
    residents: "Robby Benson",
    guests: []
  }
}
```

Using Ruby, remove Belle from the town residents, and
add her to the list of guests in the castle.

Write your code here:
```ruby
attr_accessor :residents, :guests
belle = town[:residents][1]
guests = town[:guests]
town.pop("Belle")
belle << :guests

```

### Question 3

Assume you have an array of strings representing friend's names:

```ruby
friends = ["Chip Potts", "Cogsworth", "Lumière", "Mrs. Potts"]
```

Using `.each` AND string interpolation, produce output (using `puts`) like so:

```
Belle is friends with Chip Potts
Belle is friends with Cogsworth
Belle is friends with Lumière
Belle is friends with Mrs. Potts
```

Write your code here:
```ruby
class Friends
  attr_accessor :friends

  def initialize = friends
    @friends =friends
    friends = ["Chip Potts", "Cogsworth", "Lumière", "Mrs. Potts"]
  end

  def greeting friends
    @friends.each do |friend|
    puts "Belle is friends with #{@friends}"
  end

end

chip = Friends.new "Chip Potts"
cogs = Friends.new "Cogsworth"
lumi = Friends.new "Lumière"
mrs = Friends.new "Mrs. Potts"
```
## Ruby OOP (meets Lion King)

### Question 4

Create ruby classes for `Animal` and `Lion`.
Each `Animal` should have:

- a `name` attribute
- a `greet` instance method
- Getter and setter for `name`

Create a new `Animal` instance with the name "Pumba"

Make the `Lion` inherit from the `Animal` class.
The `Lion` class should have a `pack` class variable that holds references to each instance created.

Each lion should have:
- a `king` attribute which is a boolean
  - If the instance's `name` is `Simba` make the `king` attribute true

Create a new lion instance with the name `simba`

```ruby
class Animal

  attr_accessor :name
  def initialize name
    @name = name
  end

  def greet
    puts "Hello! I'm a #{@name}!"
  end
end

pumba = Animal.new "Pumba"

class Lion < Animal
  attr_accessor :name, :king
  @@pack = []
  @king = king
  def initialize name
    @@pack << self
    @king = false
    if name == "Simba"
      @king == true
    elsif false
    end    
  end
end

simba = Lion.new "Simba"

```

## SQL, Databases, and ActiveRecord (meets Aladdin)

### Question 5

Describe what an ERD is, and why we create them for applications. Also give an
example what the attributes and relationships might be for the following
entities (no need to draw an ERD):
* Genie
* Lamp
* Person
* Pet

Your answer:
```
An ERD is an Entity Relationship Diagram which refers to the visual representation of the relationships of data sets.  Data sets can have a one-to-one relationship where they are only attributes of each other, one-to-many where a location has many cohorts and can be an attribute to many, and many-to-many when many attributes can be connected to a number of others.

In the example above, the genie has a one-to-many relationship with the Lamp and the Person and visa versa, but the Pet has a one-to-one relationship with the Person.

```

### Question 6

Describe what a schema is, and how we represent a one-to-many relationship in a
SQL database. If you need an example, you can use: people and wishes
(one-to-many).

Your answer:
```
Replace this with your answer
```
