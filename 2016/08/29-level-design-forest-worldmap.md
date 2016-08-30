# SuperTux Worldmap Design: Forest Island

SuperTux Level Design Team meeting, held on August 29, 2016 in an Etherpad document.

### Attendants

- @Rusty-Box (@SuperTux/level-designers)
- @serano01 (@SuperTux/level-designers)
- @maxteufel (@SuperTux/core)

### Decisions/Summary

- Based on RustyBox's submission for the worldmap contest. Voted on in issue SuperTux/data#24.
- Number of levels:
  - Ideally the Forest World will contain 25 levels (agreed: @RustyBox, @serano, @mt) (proposal: @RustyBox)
  - In case more or less content is required, min: 20, max: 30 (so ±5 from ideal) (agreed: @RustyBox, @serano, @mt) (proposal: @mt)
- Secret and alternate exits
  - In hidden areas: can stay with one path continuing for now. (agreed: @RustyBox, @serano, @mt) (proposed: @mt)
  - Visible while playing, but possibly still in a secret area: Place on a fork. (agreed @SuperTux/level-designers, @mt), (proposed: @mt)
- Merge ice tiles tileset and normal tileset
  - Contact LMH about this because he already uses a merged version (but outdated probably) in his add-on
- Tile requests:
    - Dark forest worldmap tiles without river required for transition
    - Ghost Forest worldmap tiles matching the new, blue-grass style from the levels
    - Ghost Forest style from <http://supertux.lethargik.org/wiki/File:Forestworldoverview.jpg> will be used later for Wasteland, no need for requests
    - Mountain worldmap tiles, similar to those of Icy Island
    - "Slope" tiles for the worldmap too, to create an illusion of height on the Forest Island.
    - Small forest castle tiles (Brown castle variant as well as Dark Forest Keep castle variant) (already discussed before)
- Remove World\_of\_Ghost.stl  ghostly.stl  Walking\_Flames.stl, The Origin of the Ghost Forest, the old castle levels, CounterCurrent.stl
- Temporarily fix castle by using icy island castle tiles. Use no castle tiles for the keys.


### Discussion

ideas anyone?

[2016-08-29 18:20 UTC+2: mt: as of now, there don't seem to be any news ideas and RustyBox is already working on the worldmap like we discussed it now. I will export this document and add it to the SuperTux/meeting repository where it can be retrieved in the future]

- mt: @RustyBox: are you aware where Bye Bye Forest is supposed to be placed?
RustyBox: I guess at the end of the whole forest worldmap
mt: Indeed. So there will need to be a transition from Ghost Forest to normal Forest with coastal area at the end. Or the level will be placed on a small island on the coast. That's your choice.
[CLOSED]

- mt: @RustyBox: currently the forest-redesign branch includes some levels I suspect you want to have removed. Which ones? <https://github.com/SuperTux/data/tree/forest-redesign/levels/world2>
RustyBox: World\_of\_Ghost.stl  ghostly.stl  Walking\_Flames.stl (And the old castle entrance (the one with the keys))  That's all for now. For more we have to wait after the poll.
mt: I don't want to break the worldmap so can you at least temporarily fix it by removing the old level dots and adding the new ones to the path?
RustyBox: I can do that.
mt: What about the tree boss level (The Origin of the Ghost Forest). I'd prefer not to have this in the Forest Island until we have a solution for the Forest boss.
RustyBox: Than it can be removed to, but I keep the level in my level folder.
mt: Unless I rebase history to specifically remove it from history git will remember it forever, but keeping a separate copy is something I can recommend too.
mt suspects serano also wants some levels to be removed from that folder I linked to. (More specifically, CounterCurrent.stl; serano, can you approve that?)
RustyBox: We can also remove the old castle levels. I guess?
mt: @RustyBox: yes, but then you need to fix the worldmap temporarily with an icy island castle for the castle. and the castles for the keys should be removed.
RustyBox: Then I'll do it.
mt: I want to have the worldmap before I remove the levels from the folder, though.
RustyBox: I know.
Serano: Yes, countercurrent can be removed
[CLOSED]

- mt: Level Distribution: We have 25 level slots available. How do we want to distribute them? I think this also partly depends on the result of the poll.
RustyBox: We should wait for that after the poll
Serano: I agree with RustyBox
[CLOSED]

How about some "slopes" (I don't know how to call that), so the forest island doesn't look just like a flat island.
  mt agrees, as usually
  Serano agrees
  [CLOSED]

-Serano: We could need some mountain tiles for the worldmap if we want to show that Tux is now entering the underground forest
  mt: I like the idea of Forest mountains in general, because tile variance and we have them in Icy Island too. Just some few mountain tiles like in Icy Island because this is not the Land of the Mountain Range
  RustyBox: Sounds good.
  mt: [CLOSED]

- RustyBox thinks that maybe using the normal level dots is better instead of the shroom dots
Serano: I like the shrooms. They give an unique touch to the world
mt agrees with Serano.
RustyBox: Do they even look like shrooms? They look more like "portals" to me. Also, then we could need a bonus variant (like the blue dot in icy island bonus)
mt: They do look like shrooms and I like the look for the forest island.
Serano: So requesting a special dot for the bonus levels, then, too?
mt: What if we "color corrected" the current shroom dots and add some spikes? That would at least be a temporary solution. For a custom one, I could imagine a wooden structure, similar to wooden jumpy.
Serano: Maybe to keep in style and make a blue and shiny shroom-dot for this purpose
mt: I suggest we just request a bonus leveldot for Forest Island and leave the details to be defined by the artist.
Serano: I agree
[CLOSED]

- What about a different music for the ghost forest worldmap area?
  - Good idea. Agreed. Ask wansti and krobonil if everyone agrees.
  - Serano: I like the idea, too
  - mt: Also needs some scripting or implementation in the game.
  [CLOSED]

- mt: (low priority idea): names for Forest Island in general and Haunted/Ghost Forest?
RustyBox: Do you mean that both have a different name?
mt: @RustyBox: Forest Island in general could have a name. Like a country. Then think of Ghost Forest, with a separate name as a federal state or so.
Serano: Something like woody island perhaps?
mt: @Serano: yes. Or more adjectives... Forests of the ...; Island of the ... Forest

- mt thinks that using the "Ghost Forest" tiles for dark forest is confusing
RustyBox: We need a better "transition" for the dark forest, so there don't has to be a river between them.
mt: @RustyBox: do we need tiles for that?
RustyBox: @mt: Yes.
mt: @RustyBox: So as a result of this document we will prepare a list of urgently needed worldmap tiles. Someone will have to present that to grumbel.
mt: @RustyBox: That means you agree with my thinking? @serano what do you think?
RustyBox: Yes.
Serano: okay
[CLOSED]

- mt: I'm bringing up another related topic to above, do we want to use the current Ghost Forest tiles for darker forest instead and request new Ghost Forest/actual wasteland tiles?
RustyBox: Yes. that would be good.
Serano: yes, so it fits better to the actual ghostforest levels
mt: I'd suggest on one hand for the levels and on the other hand for the worldmaps: I actually like this Ghost Forest style: http://supertux.lethargik.org/wiki/File:Forestworldoverview.jpg
RustyBox: Well, I like both styles. (mt: yes, I like both as well. Maybe two different styles of Ghost Forest (level and worldmap) tiles.)
Serano: I'd say we use this style later for some kind of desert world
RustyBox: The other style fits more a wastleland
mt: The wasteland thing is true so we reserve it for a separate world. That means we need Ghost Forest tiles matching the current worldmap tiles.

- Should RustyBox's worldmap base be edited so it contains multiple different islands, or is the current form okay. "Forest Islands" would also be interesting. On the other hand, that could be reserved for the subtropical ocean world to have more water in the worldmap. Anyway I think water should be in the worldmap (and ponds) for variance of tiles.
Serano: True, Tropical Islands would be more fitting instead of the forest one.
RustyBox: The forest is just not the right place for smaller island.
mt: Yes indeed. So discard that idea. Do you agree about using more water *in the worldmap*.
Yes, it brings some more variation in it.
mt: Anyone have more ideas on this, or can we move it?
RustyBox: I say we can move it.
Serano: yeah let's move it

-  RustyBox: In addition, we have to make it possible to use the forest worldmap tiles with the new animated water for the worldmap
  mt: already opened an issue, that doesn't require artist involvement but someone who understands the tileset format. I think Hume2 might be able to do that.
    RustyBox: There was an add on that uses some forest tiles with the new water. I think it was matties world.
    Are you sure it uses them in the same, very same *worldmap*?
    RustyBox: Yes. There is a secret level on that worldmap, that was a forest level, instead of an ice level. It's on a tiny forest "island"
    Indeed.
    RustyBox: We could use them
     Problem is that the current tilesets have been updated meanwhile. I suggest we contact LMH LMH 0013 or so on GitHub [and at gmail dot com] and ask him to merge a current version of that.

- Serano: We also need more background tiles for the ghostforest levels
 different discussion
 mt: also prepare a document for grumbel
 but let's focus on the worldmap, see the title of this document: SuperTux Worldmap Design: Forest Island
 Can I move that to the section below?
 Serano: yes, go ahead

- We need to know how many levels the forest world is supposed to have
  mt: min 25, ideally 30, max 35 - we should plan for the "ideal" value. bonus levels or such stuff can be added later if it doesn't exceed 35 levels
 RustyBox: I would say the ideal value should be ~25 levels (comment: mt: I don't think you should approximate ideal values. You should set one and then that won't be changed)
 RustyBox: Then I would say 25
 mt if no one shows up later and suggests sth else I'd agree on 26: 20 normal levels, 2 castle levels, 4 special levels (with collectibles (current "keys"))
 mt: reason for 26 not 25: 3 special levels are certainly not enough (okay it doesn't have to be exactly 20 normal levels either)
 serano:I'd like 30 levels per world, in icyisland there are currently 29, seems like a good value to me
 mt: @serano: would you be okay with 25 or 26 ±5 levels (then we'd be at least 20 or 21 levels and at most 30 or 31 levels)
Yes, that would be fine by me
mt: @RustyBox: with what do you agree? do you stay at 25 or agree with 26?
RustyBox: I stay at 25. Not every world has to have 20 normals or 4 special levels. Some worlds could have maybe 19 normal and 5 special.
mt: @RustyBox: we're talking about forest world specifically now. But okay, 25 ± 5 is okay with me.
Serano: So okay, 25 levels, 5 of them have an secret exit which lead to the bonus levels then?
mt: No. ±5 means it can be 5 more or 5 less than 25 if we need to add more/remove content
mt: @RustyBox, @serano: agree with the ±5 as well? I'd be okay with 25 = ideal.
RustyBox: @mt: I agree with that.
Serano: Me too

- Which or how many levels are going to have a second or secret exit? 
  mt: we don't want too many alternate paths (alternate paths are not even implemented right now, and I'm not sure if they will be in 0.6)
   RustyBox: I wanted to know for forks in the worldmap
    mt: right, that is a problem right now. because until we have implemented that they will just show up as random forks in the road. I suggest we put them at strategically important places, such as before or in castles, and special levels (and one for a bonus level - Owls' Revenge possibly)
    Sounds good (yay, I can type again)
     RustyBox: @mt: Why do we need secret or a second exit in a castle?
     mt: Okay not in a castle. But before the castle it could be useful to gather bonuses. And if we have more than two worlds skipping one castle or so might be a possibility.
    RustyBox: I'm not sure if we should make it possible to skip castles.
    mt: Anyway, let's reserve us the option of second/secret exits so you can have less linearity even with some story in it. If you need to look for secret exits it makes the level way more interesting and that unlocking a different path on the worldmap makes you want search for such an exit.
  Serano: Especially for keys, right?  
  mt: Well we could make it so keys are only available to play when having unlocked a secret path or so. Also, we can ignore secret paths for now. But please for all updated levels add the possibility of adding many secret areas. Because then a secret exit could just be added without anyone noticing anything.
  RustyBox: We might need a new purpose for the keys, because we don't have a locked castle door anymore.
 mt: @RustyBox: well, we will require collectibles to enter the castle. and we can add a cutscene for that (cutscenes don't add to the level count, come on)
 RustyBox: But I would say we should use a "different" kind of key, because five keys and also creating the word NOLOK feels a bit like a final
 mt: I agree. I'd suggest one or two collectibles. It could be a magic lantern you get in the ghost forest and something else. Other collectibles should be placed in forest world too, though, which can be used elsewhere (shop, final castle).
 serano: One or two keys are sufficient, I think.
 mt: @serano: don't think in keys, it will be collectibles
 serano: @mt: Do you mean collectibles for the inventory?
 mt: @serano: right. they will replace keys. that will be easier than scripting the inventory system.
 RustyBox: We have to generelly think about other collectibles in the future
 mt: Going away from keys also has the advantage of being able to use more fitting collectibles. I.e. for "Shocking" we could add a Trident (/Dreizack/ now, Triton would be another god) as collectible, instead of a blue key.
 RustyBox: That's right.
 mt: So secret exits. For now, levels with them not visible can just stay like that somewhere in the worldmap (a different path can be added later on). Levels with visible second exit should be at a fork that already exists (in the future behavior might be changed so it appears that different paths of the fork are unlocked depending on which way you take). Agree with that?
 RustyBox: Sounds good. Paths that aren't unlocked could be for example transparent.
 Serano: I agree
 mt: @RustyBox: yea but that's something for the future. we need a major rewrite of worldmaps for that, I suppose.
