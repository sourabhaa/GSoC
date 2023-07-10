Maintain and Port Sugar Activities to Flatpak
-----

***Google Summer of Code, 2023***

*Name - Sparsh Goenka*

*Email - sparshgoenka@gmail.com*

*GitHub username - [sparshg](https://github.com/sparshg/)*

*Mentor - [Martin Abente Lahaye](https://github.com/tchx84), [Ibiam Chihurumnaya](https://github.com/chimosky/)*

Reaching mid-evaluation for my project, I have learned a lot and helped to update the sugar activities to Flatpak.
Here is a list of changes I have made till now:

## Activities updated

| #   | **Flatpak Package** | **Pull Requests**                                                                                                 | **Status** | **Comments**                                                                                                            |
|-----|:-------------------:|-------------------------------------------------------------------------------------------------------------------|:----------:|-------------------------------------------------------------------------------------------------------------------------|
| 1.  |        Pippy        | Upstream:<br> [Fix pygame full screen issue in some examples](https://github.com/sugarlabs/Pippy/pull/86)         |   Merged   | Issue noticed after updating flatpak to pygame 2                                                                        |
|     |                     | Upstream:<br> [Fix undo and redo remaining sensitive](https://github.com/sugarlabs/Pippy/pull/89)                 |   Merged   | Closed [#68](https://github.com/sugarlabs/Pippy/issues/68) and [#69](https://github.com/sugarlabs/Pippy/issues/69)      |
|     |                     | Upstream:<br> [Check box2d installation when loading box2d example](https://github.com/sugarlabs/Pippy/pull/90)   |   Merged   | Closed [#66](https://github.com/sugarlabs/Pippy/issues/66)                                                              |
|     |                     | Upstream:<br> [v76](https://github.com/sugarlabs/Pippy/pull/88)                                                   |   Merged   |                                                                                                                         |
|     |                     | Shared Modules Upstream:<br> [Add pygame 2](https://github.com/flathub/shared-modules/pull/247)                   |    Open    | Doesn't seem like this will merge soon, maintainers suggest including it in BaseApp if build times are relatively small |
|     |                     | [Update Pippy](https://github.com/flathub/org.sugarlabs.Pippy/pull/6)                                             |   Merged   |                                                                                                                         |
| 2.  |       Finance       | [Update BaseApp and add data checker](https://github.com/flathub/org.sugarlabs.Finance/pull/4)                    |   Merged   |                                                                                                                         |
| 3.  |        Words        | [Update activity and BaseApp](https://github.com/flathub/org.sugarlabs.Words/pull/5)                              |   Merged   | Included WebKit2 patch to update                                                                                        |
|     |                     | [Add data-checker to gst-plugins-espeak](https://github.com/flathub/org.sugarlabs.Words/pull/7)                   |   Merged   |                                                                                                                         |
| 4.  |         Maze        | [Update activity and BaseApp](https://github.com/flathub/org.sugarlabs.Maze/pull/6)                               |   Merged   |                                                                                                                         |
| 5.  |        Abacus       | [Update activity and BaseApp to 23.06](https://github.com/flathub/org.sugarlabs.AbacusActivity/pull/9)            |   Merged   |                                                                                                                         |
| 6.  |     Turtle Pond     | [Update activity and BaseApp](https://github.com/flathub/org.sugarlabs.TurtlePondActivity/pull/5)                 |   Merged   |                                                                                                                         |
| 7.  |     Slide Ruler     | [Update BaseApp and add data-checker to activity](https://github.com/flathub/org.sugarlabs.Sliderule/pull/4)      |   Merged   |                                                                                                                         |
| 8.  |    Music Keyboard   | [Update](https://github.com/flathub/org.sugarlabs.MusicKeyboard/pull/7)                                           |   Merged   | Added environment variables while building csound to include ctcsound.py. Removed ctcsound from sources                 |
| 9.  |        Story        | [Update](https://github.com/flathub/org.sugarlabs.StoryActivity/pull/5)                                           |   Merged   |                                                                                                                         |
| 10. |      ReadETexts     | Upstream:<br> [Fix: Activity fails to run with ValueError](https://github.com/sugarlabs/readetexts/pull/22)       |   Merged   |                                                                                                                         |
|     |                     | Upstream:<br> [v23](https://github.com/sugarlabs/readetexts/pull/23)                                              |   Merged   | Closed [#21](https://github.com/sugarlabs/readetexts/pull/21)                                                           |
|     |                     | [Update](https://github.com/flathub/org.sugarlabs.ReadETexts/pull/5)                                              |   Merged   |                                                                                                                         |
|     |                     | [manifest: Update and Apply data-checker to activity](https://github.com/flathub/org.sugarlabs.ReadETexts/pull/7) |    Open    | Closed [#6](https://github.com/flathub/org.sugarlabs.ReadETexts/pull/6)                                                 |
| 11. |        Chart        | [Update to BaseApp 23.06 and add data checker](https://github.com/flathub/org.sugarlabs.Chart/pull/4)             |    Open    | ~Issue in upstream with icon not being square~, added patch                                                             |
| 12. |       Implode       | [Update to BaseApp 23.06 and Apply data-checker](https://github.com/flathub/org.sugarlabs.ImplodeActivity/pull/4) |    Open    |                                                                                                                         |
| 13. |    Color Deducto    | [Update BaseApp and add data-checkers](https://github.com/flathub/org.sugarlabs.ColorDeducto/pull/5)              |    Open    |                                                                                                                         |
| 14. |       Measure       | [Update dependencies and add data-checkers](https://github.com/flathub/org.sugarlabs.Measure/pull/5)              |    Open    |                                                                                                                         |

## Activities Ported
| #   | **Flatpak Package** | **Pull Requests**                                                                                                 | **Status** | **Comments**                                                                                                            |
|-----|:-------------------:|-------------------------------------------------------------------------------------------------------------------|:----------:|-------------------------------------------------------------------------------------------------------------------------|
| 1.  |     [TicTacToe](https://github.com/sparshg/org.sugarlabs.TicTacToe-flathub)      | Upstream:<br> [Fix stop button not working](https://github.com/sugarlabs/tictactoe/pull/6)                        |   Merged   | There was an issue with Flatpak package not closing when stop button is clicked                                         |
|     |                                                                                  | Upstream:<br> [Fix X and O are disappearing randomly](https://github.com/sugarlabs/tictactoe/pull/9)              |   Merged   | There was this glitch when pygame canvas had a height with odd number of pixels                                         |
|     |                                                                                  | Upstream:<br> [Add screenshots and v3](https://github.com/sugarlabs/tictactoe/pull/10)                            |   Merged   | Warning due to the existing help image being too wide when used as Flatpak "screenshot" in activity.info                |
| 2.  |[Block Party](https://github.com/sparshg/org.sugarlabs.BlockPartyActivity-flathub)| Upstream (Issue):<br> [New Tagged Release](https://github.com/sugarlabs/block-party-activity/issues/35)                   |  Resolved  |                                                                                                                         |

## Other
| #   | **Flatpak Package** | **Pull Requests**                                                                                                 | **Status** | **Comments**                                                                                                            |
|-----|:-------------------:|-------------------------------------------------------------------------------------------------------------------|:----------:|-------------------------------------------------------------------------------------------------------------------------|
| 1.  |       BaseApp       | [Downgrade TelepathyGLib](https://github.com/flathub/org.sugarlabs.BaseApp/pull/8)                                |   Merged   |                                                                                                                         |

Thanks to my mentors for their guidance and many useful tips, I have been enjoying working with them! I will try porting more new packages to Flatpak in the coming month too.