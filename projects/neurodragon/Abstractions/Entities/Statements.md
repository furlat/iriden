`AtomicStatements` are logical representation associated to [[Entities]] [[Attributes]]. They are composed by a tuple `(attribute,truth_value)` and are used to associate an attribute to a specific truth value. Continuous and structured attributes are converted to a set of bools to enable a statement representation by the underlying primitives.

`CompositeStatement` are hash maps or dictionaries of statements `{attribute: truth_value}` and are used to define conditions across multiple attributes that must be `ALL` valid simultaneously.

