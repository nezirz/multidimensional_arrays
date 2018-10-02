# README

Simple project for showing how to save multidimensional array to db with ruby on rails.

Important step is to define migration field as a string and add `:array => true` attribute to migration field.

Sample post migration:
```ruby
class CreatePosts < ActiveRecord::Migration[5.2]
  def change
    create_table :posts do |t|
      t.string :title
      t.string :body, :array => true

      t.timestamps
    end
  end
end
```


![alt text](https://raw.github.com/nezirz/multidimensional_arrays/master/MultidimensionalArrays.png)
