**Lua** is a programming language that is integrated into the *Kenshi*
Wiki with [Scribunto](mw:Extension:Scribunto "wikilink"). Lua source
code is run from Modules in their own namespace, and invoked with
`{{#invoke:Module|function}}`; this should done with a wrapper template.
For example, if we have a module named "foo", then we should have a
template called "Template:Foo" consisting of `{{#invoke:Foo|main}}` to
call the module, and use `{{Foo}}` to use the module on pages.

For certain complex templates, Lua runs many times more efficiently than
standard wikitext. It can also perform operations not available
otherwise in wikitext. Unlike JavaScript, it is available to all
readers, and does not need to be enabled. It is also run during parsing,
rather than after.

All templates that directly invoke modules should be marked with the
template.

## See also

- [Wikipedia:Lua (programming
  language)](Wikipedia:Lua_(programming_language) "wikilink") and
  [Wikipedia:Project:Lua](Wikipedia:Project:Lua "wikilink"), for a more
  in-depth breakdown of the coding Language
- [mw:Extension:Scribunto/Lua reference
  manual](mw:Extension:Scribunto/Lua_reference_manual "wikilink"), for
  the documentation of Lua as used by the Scribunto extension
- [Special:PrefixIndex/Module:](Special:PrefixIndex/Module: "wikilink"),
  for a list of all current modules
- [RuneScape:Lua/Modules](RuneScape:Lua/Modules "wikilink"), for a list
  of all modules, excluding Exchange and miscellaneous data pages
- [RuneScape:Lua/Helper
  modules](RuneScape:Lua/Helper_modules "wikilink"), for a table of
  modules designed to facilitate writing other modules
- [:Category:Lua-based
  templates](:Category:Lua-based_templates "wikilink"), for an index of
  templates that directly invoke Lua

[Lua-based_templates](Category:Lua-based_templates "wikilink")