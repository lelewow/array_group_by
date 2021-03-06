# array_group_by

`array_group_by` is a function that groups an array by a key or set of keys
shared between all array members.

# Usage

Example input:

``` php
$records = array(
    array(
        "state" => "IN",
        "city" => "Indianapolis",
        "object" => "School bus"
    ),
    array(
        "state" => "IN",
        "city" => "Indianapolis",
        "object" => "Manhole"
    ),
    array(
        "state" => "IN",
        "city" => "Plainfield",
        "object" => "Basketball"
    ),
    array(
        "state" => "CA",
        "city" => "San Diego",
        "object" => "Light bulb"
    ),
    array(
        "state" => "CA",
        "city" => "Mountain View",
        "object" => "Space pen"
    )
);

$grouped = array_group_by($records, "state", "city");
```

Example output:

``` text
Array
(
    [IN] => Array
        (
            [Indianapolis] => Array
                (
                    [0] => Array
                        (
                            [state] => IN
                            [city] => Indianapolis
                            [object] => School bus
                        )

                    [1] => Array
                        (
                            [state] => IN
                            [city] => Indianapolis
                            [object] => Manhole
                        )

                )

            [Plainfield] => Array
                (
                    [0] => Array
                        (
                            [state] => IN
                            [city] => Plainfield
                            [object] => Basketball
                        )

                )

        )

    [CA] => Array
        (
            [San Diego] => Array
                (
                    [0] => Array
                        (
                            [state] => CA
                            [city] => San Diego
                            [object] => Light bulb
                        )

                )

            [Mountain View] => Array
                (
                    [0] => Array
                        (
                            [state] => CA
                            [city] => Mountain View
                            [object] => Space pen
                        )

                )

        )
)
```

# Installation

A Composer package is available for this function. Just add the following to
`composer.json`.

``` javascript
{
    "require": {
        "jakezatecky/array_group_by": "~0.7.2"
    }
}
```

Alternatively, you can just include the `src/array_group_by.php` file.
