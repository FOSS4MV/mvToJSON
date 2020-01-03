# MV.TO.JSON

Use this little code snippet in your subroutines or functions to convert a given MV dynamic array and associated metadata (*see example TEST.MV.TO.JSON*) to correctly formatted JavaScript Object Notation (JSON).

This code **only formats** the dynamic array to JSON. Other than string/numeric type checking, it is your own code must consider escaping string values such as quotations marks, slashes, backslashes, etc.

This code will infer JavaScript arrays from multivalues and arrays of arrays from subvalues, but without those markers present, it will not create a JS array where one might be desired. 

An example would be an attribute that represents multivalued data, but only contains a single value. MV.TO.JSON
will only add the single value to the JSON output.

Of course, this limitation is easily overcome by making your own updates to the metadata format & processing.  If you do something interesting, consider contributing your changes here.

Testing has only been done with D3, but the code should be generic enough to work on most any MV platform.