`<noinclude>`This template describes the **delay** [parameter](../_uncategorized/EventMacro.md#parameters) of the automacro eventMacros.`</noinclude>`

delay <[seconds](References.md#seconds)\>

- **delay** is an optional parameter.
- **delay** defines the time in seconds to wait before executing the macro in call parameter.
- If not used in the automacro the default value will be used, which is: 0.
- Must have a numeric value.
<!-- -->

    automacro <automacro name> {
        <automacro conditions and parameters (and only them)>
        delay 5
        call myMacro
    }
    macro myMacro {
        <macro instructions (and only them, as this is regular macro)>
        log This is being logged 5 seconds after the automacro activated
    }