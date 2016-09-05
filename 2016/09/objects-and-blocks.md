## Discussion of blocks and objects

mt and I (Karkus) had the following discussion on the 5th of September, at 13:36 UST.

**This was not during a meeting**

We discussed the problem of managing blocks, and noted how when tiles are placed in the level, they are sometimes converted into objects when the level is loaded. This hides some implementation from the level designer, which we considered unnecessary.

```
<mteufel[m]> [idea] level finish music that depends on the world you're in
<Karkus>     mteufel[m]: Good idea.
<Karkus>     But maybe not so easy.
<mteufel[m]> Karkus: you think so?
<Karkus>     mteufel[m]: You could do it per-worldmap, but what if we merge the worldmaps? You could do it per-level, but what object will you apply it to? You can't do it per finish, because finishes aren't objects (yet)
<Karkus>     You could do it per-sector, but that's messy/
<mteufel[m]> Karkus: per-sector
<Karkus>     I think we should make  finishes objects.
<mteufel[m]> GameSession::start_sequence got currentsector as a variable
<mt>         Karkus: I think sequences should be objects
<mt>         well, they already are
<mt>         we have sequence triggers
<Karkus>     sequences and also finishes, and also worldmap paths
<Karkus>     should all be objects
<mt>         Karkus: "finishes" are a combination of two special tiles:
<mt>         or one normal tile, the pole tiles
<Karkus>     I know
<mt>         and special tiles, the sequence triggers
<mt>         but there is also an object "sequence trigger"
<Karkus>     They have start sequence and end level, or something like that.
<Karkus>     Oh.
<mt>         poles should continue to be tiles
<mt>         that allows z-index flexibility
<mt>         with a single sprite, it would be fixed to one z-index otherwise
<mt>         but we should get rid of special tiles
<mt>         because what happens with them is simple
<mt>         upon reading, the sector parsing code transforms them into an applicable object
<mt>         similar to the "block tiles" and the "coin tiles"
<mt>         we should get rid of these too
<mt>         and our current sequence code is stupid anyway
<mt>         it assumes a sequence is one of the last parts of a level
<mt>         it just sets the level to won, regardless of what sequence is played
<mt>         currentsector->get_players()[0]->get_physic()->/* ... */
<mt>         I like how our code basically contains support for multiplayer already
<Karkus>     I don't think we should get rid of block tiles, personally, because they are quite useful. We should get rid of special tiles, that's for sure.
<mt>         Karkus: block and coin tiles are special tiles too
<mt>         they spawn an object
<Karkus>     mt: Well, we should get rid of sequence and finish tiles.
<Karkus>     But not block object tile things.
<Karkus>     nor coins.
<mt>         finish is also a sequence
<mt>         Karkus: they are useful in the editor
<mt>         but they're just specially treated parts of the code
<mt>         specially treated parts of the code, when you have other infrastructure where they wouldn't need special treatment, are always bad
<mt>         it's more code to maintain, and it can introduce more security problems
<Karkus>     mt: We should keep them as they are in the editor. Implementation aside.
<Karkus>     They should be grid locked, and easy to place
<mt>         all objects need to be grid locked
<Karkus>     Objects are a real pain to work with atm.
<mt>         well, not locked per se
<mt>         but locked if the user wants them to be locked
```
