### What are the five variable types in Terraform?

- string
- number
- bool
- list
- map

### Write the variable precedence order from lowest to highest priority.

- Default values: Defined in variables.tf file
- Environment variables: Defined in CLI using export command like "export TF_VAR_instance_type="t3.small""
- terraform.tfvars: Overrides above settings
- terraform.tfvars.json: This takes the precedence above terraform.tfvars
- *.auto.tfvars: Files ending with .auto.tfvars override other file types above
- -var-file Flags: This type of flag mentioned override all other files
- -var Flags: This flag has the highest priority

### Pick five functions you find most useful and explain what each does.

- lookup(map, key, default): Retrieves value of an element from map by providing a key
- templatefile(path, vars): Reads a file local filesystem and renders its content as a string, substituting variables in var map.
- merge(map1, map2, ...): Combines multiple maps into a single map
- flatten(list): Takes a list that contains nested list, replaces them with flat sequence of all the elements, replacing nesting
- try(expression 1, expression 2, ...): Evaluates a series of expressions and returns the result of first one that doesn't returns error.

### Difference between variable, local, output and data

- **variable**: All values are defined here so that it can be called directly from other files
- **local**: They are same as variables which are defined in a module and can be accessed in the module itself
- **output**: Print the output of specific values after it has been provisioned
- **data**:  Used to fetch information from external system or existing infrastructure which is not part of current one