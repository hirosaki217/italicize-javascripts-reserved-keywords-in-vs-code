// im found it from https://stackoverflow.com/questions/51110201/italicize-javascripts-reserved-keywords-in-vs-code and save it
{
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "scope": [
                    // all comment types
                    "comment",
                    // true, false, null
                    "constant.language",
                    // import, from, export, default, return, if, for, break, continue, try, catch, finally,
                    // throw, default, yield, await
                    "keyword.control",
                    // in, void, delete, instanceof
                    "keyword.operator.expression",
                    // debugger
                    "keyword.other",
                    // new
                    "keyword.operator.new",
                    // super, this, arguments
                    "variable.language",
                    // attributes in html, jsx, etc.
                    "entity.other.attribute-name",
                    // static, extends, async, private, public, implements
                    // constructor, const, let, var, enum, class, function, interface
                    // no explicit scopes for constructor, const, let, var
                    // also no explicit scope for function without the arrow
                    // therefore we enable all storage and explictly exclude the arrow in another scope
                    "storage",
                    // // no explicit scope for the eval keyword yet
                    // // can be targeted with the scope below, but scope is too broad
                    // "support.function",
                    // // no explicit scope for the package keyword yet
                    // // can be targeted with the scope below, but scope is too broad
                    // "variable.other.readwrite",
                ],
                "settings": {
                    "fontStyle": "italic"
                }
            },
            {
                "scope": [
                    // function keyword does not have an explicit scope without the arrow
                    // therefore we explictly exclude the function arrow from being italicized
                    "storage.type.function.arrow",
                ],
                "settings": {
                    "fontStyle": ""
                }
            }
        ]
    }
}
