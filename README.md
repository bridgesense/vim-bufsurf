| WARNING: This is not the original repo. Go [here](https://github.com/ton/vim-bufsurf) for the version by Ton van den Heuvel|
| --- |

*This version shares the surf history of all windows.  Since this includes quite a bit more activity, an additional option (see documentation) has been added that limits the number of historical references. The oldest entries are pruned first depending on the current position in the index.*


vim-bufsurf
-----------

This plugin enables surfing through buffers based on a viewing history per
window.

When editing multiple files oftentimes it would be nice to be able to go back
and forth between the last edited files, just like a web browser allows the
user to navigate web pages forward and backward in history. The standard
`:bn(ext)` and `:bp(revious)` Vim commands allow to switch between next and
previous buffers respectively, but they do no take into account the history of
the last used files. Instead, they use the order in which the files were
opened, which can cause confusion in case the user expects to navigate forward
and backwards in history.  For example, in case the user opened the files `A`,
`B`, and `C` in the following order:

1. `A`
2. `B`
3. `C`

and the navigation history would be:

1. `A`
2. `B`
3. `C`
4. `B`

then `:bp(revious)` in the last buffer (containing `B`) would open up buffer
`A`, where `C` is preferable. This plugin supplies the user with the commands
`:BufSurfForward` and `:BufSurfBack` to navigate buffers forwards and backwards
according to the navigation history.
