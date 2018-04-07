ComSenMod 3.4
By ‘Crater Creator’
Last tested with Alpha 16.4 b8 (Stable)

As I’ve played 7 Days to Die for hundreds of hours, I’ve accumulated a growing laundry list of questions.
Why do you never find clothes in a suitcase?
Shouldn’t wearing shorts make you warmer than wearing nothing?
What am I supposed to do with this 1 nail I found?

And so on.  Eventually, I decided to adjust the files myself to address as many imbalances, omissions, and peculiarities as I could.  My criteria has been to only make a change when A) there’s a good reason; and B) I understand the consequences downstream.  Practically speaking, most of the changes relate to loot, with a bit more authentic survival thrown in, too.

The mod’s focus is not on making the game easier or harder.  Nor is it meant to cater to any one playstyle.  It’s simply designed to inject more common sense into the game.  Hence “ComSenMod”, short for Common Sense Mod.

My hope is that ComSenMod gains broad appeal: that players will wonder why the game wasn’t always this way.  Who knows, it may even give the developers some things to think about.  My second hope is that if you try ComSenMod, you’ll let me know what you think.  I’ve tested it extensively for balance in single player and coop games.  I’m open to additions and improvements, especially along the lines of “I used ComSenMod in X kind of game for Y long and there’s too much/too little of Z.”

ComSenMod works like other mods: to install, drag and drop the contents of the Config folder into your installation’s Config folder, replacing the existing files.  ComSenMod is also compatible with the 7DtD Mod Launcher To uninstall, you can verify the integrity of your game files in Steam.  To use ComSenMod with other mods, you’ll have to merge any conflicting files together yourself.

Change List

This is a list of all changes in ComSenMod relative to the vanilla game.  For your reading pleasure, each change is accompanied by the reasoning behind it.

Version 3.4	11/25/2017
* Reorganized files to work best with 7D2D Mod Launcher
* Synched files with A16.4 Stable

blocks.xml
* Set storage boxes to use new larger container definition
	They’re bigger and more expensive to make than chests, and so should offer more space

entityclasses.xml
* Scrap brass can be harvested from zombie dogs
	Representing brass dog tags, and adding more reward for killing a tough enemy
* Greatly reduced minibike hit points
	The old value wasn’t balanced, making the minibike virtually indestructible
* Narrowed the gap in hit points between basic male & basic female zombies, but reduced entity attack damage for basic female zombies
	Physical differences in e.g. upper body strength are better manifested in attack damage, rather than hit points. Unfortunately the game doesn’t support a random range of values to represent individual human variation.
* Set feral zombies to use same loot lists as their non-feral versions
	Many were using fat zombie loot, which is tailored specifically for fat zombies
* Assigned basic male & female zombies to use gender-specific loot lists
	So that, for example, males don’t carry skirts
* Reduced hit points on fat Hawaiian shirt zombies
	Unlike cop zombies, these have no special abilities, loot, or appearance of strength to support the extra hit points over other fat zombies
* Gave zombies Boe, old timer, farmer, & stripper the same hit points as other basic zombies
	These have no special abilities, loot, or appearance to support the extra hit points over other basic zombies
* Reduced burnt zombie’s hit points
	To match their new, lower quality burnt loot

items.xml
* Added handZombieFemale that does reduced damage
	If zombies are going to incorporate physical differences between males and females, let’s do it in an authentic way. Research indicates women have significantly lower upper body and grip strength, which would affect how hard they can attack with their arms, while the amount of pain or trauma they can sustain relative to men is less clear, which would affect their hit points. 

loot.xml
* Defined separate loot list for storage boxes
	They’re bigger and more expensive to make than chests, and so should offer more space
* Added empty cans to canned food loot
	Anywhere you might find canned food, you might also find an empty can
* Substituted cupboard loot in coolers with canned food loot
	Other cupboard loot, like seeds and paint, wouldn’t be found in coolers
* Changed minibike wheels found in car loot to tires
	Representing a single spare tire, instead of a set of minibike wheels
* Added eggs & feathers to mailbox loot
	A convenient place for a bird to nest in a post-apocalyptic world
* Created separate loot lists for fat male & fat female zombies & increased chance of them carrying clothes
	So that, for example, males don’t carry skirts
* Made a new ‘burnt junk’ loot list for burnt zombies and furnaces
	A lot of regular junk would be destroyed in a fire

recipes.xml
* Added recipes for flagstone gable, brick gable, wood gable, and wood pyramid
	There are holes in the full upgrade path for these shapes, but this way players can still craft the blocks that already exist
* Reduced time to forge newer brick shapes
	Applying the original adjustment to newer block shapes that hadn’t received the adjustment
* Added alternate recipes to use clean water instead of murky water
	Clean water should work just as well; players shouldn’t lose out just because they boiled all their water
* Added blueberries to paint recipe
	Red, blue, and yellow pigments are needed to create a full range of hues. Thanks, elementary school art class!

Version 3.3	9/4/2017

* Merged all ComSenMod files with updates up to Alpha 16.3 b12 (Stable)

blocks.xml
* Enabled picking up tires directly instead of destroying them
	Destroying a tire would make it unusable
* Enabled picking up hubcaps directly instead of destroying them
	Destroying a hubcap would make it unusable, plus this rewards getting up close to check suspected mines in the wasteland
* Added chance to harvest hubcaps from intact cars and air filters from partially damaged cars
	If you dismantle a whole car, you’d expect to find these car parts

buffs.xml
* Players now get steadily hotter while they’re on fire
	Fire hot!

items.xml
* Restored machete’s block damage to vanilla values
	Only the damage versus wood needed adjustment
* Increased machete damage bonus against wood
	Machetes are made to chop wood, so they should be as good at damaging wood as an iron fireaxe
* Increased fire protection from hazmat clothes
	Repurposing hazmat clothes as fireproof clothes, since radiation protection doesn’t currently impact gameplay
* Reduced economic value of hazmat clothes by a factor of 4 (about three times that of leather clothes)
	To better match their actual value as clothing, and value when scrapped
* Changed padlock material from metal to brass
	They look like brass, which is a common padlock material.  Extra padlocks should be more valuable given their rarity, and this compensates for zombies not carrying as much brass as in vanilla.
* Disabled farming tip when picking up coal
	Assumed to be an oversight, since coal isn’t used in farming
* Enabled eating snowballs directly, causing cooling and potentially dysentery
	To replace melting snow at a campfire (see recipes change)

loot.xml
* Combined quests & treasure maps into one loot group
	The tiny probabilities were too cumbersome to keep recalculating with every other change
* Removed quests & treasure maps from football, hazmat, cheerleader, skateboarder, & businessman zombies
	These zombies all drop ‘personal junk’ loot, which incorporates the chance to drop quests or treasure maps
* Standardized chance of finding a quest or treasure map from a zombie (2.7%) or container (0.75%)
	Some typical ‘everyday’ zombies, like businessmen and cheerleaders, had an extra chance for no particular reason
* Added new, separate male & female clothes groups for future use
	E.g. so male zombies don’t carry skirts
* Replaced ZU shirt in cheerleader zombie loot with tank tops
	To better reflect her appearance & reduce redundancy with football player loot
* Increased chance to find compound bow parts among basic gun loot
	They were several times rarer than common firearm parts, and found less often than whole bows in testing
* Changed lumberjack & farmer zombies to have a chance to drop all bows & bow parts
	If they’re going to carry a bow, there’s no particular reason it would have to be one bow over another
* Slightly increased chance to find magnum parts among basic gun loot
	It’s taking too long (over 140 days) to assemble a magnum in testing
* Reduced chance of finding pistol+ammo in toilets
	This was noted in version 2.5 but never actually changed
* Reduced container size of storage chests & generic chests
	The easiest container to make shouldn’t also be the biggest.  There’s still plenty of space: enough to transfer a whole backpack of stuff.
* Rebalanced all containers sizes, mostly by increasing sizes of furniture containers
	Players that want to use more than just crates or chests will get more consistent results based on each container’s size, shape, and how costly it is to craft or buy
* Added night vision goggles to military armor loot
	They could be found alongside other military gear
* Removed night vision goggles from zombie soldier loot
	He’s not visibly wearing goggles, and it’s now redundant with military armor

recipes.xml
* Replaced iron pipes in minibike seat recipe with wood & mechanical parts
	Research shows metal pipes aren’t involved.  A wooden base is typical, with bolts to mount it.
* Added nails to wooden desk recipe
	To match similar furniture, and balance better with the iron desk
* Removed wrench & hammer from workbench recipe
	Tools for the workbench are now used like tools at other stations
* Updated workbench recipes to require the wrench, wire tool, or tool & die set for large constructions, electronics, and tools/parts, respectively
	Not everything requires the same tools.  As the workbench’s role grows, it becomes more important for its utility to evolve over time, instead of having endgame capability as soon as it’s created.
* Increased forged iron required to craft lockers
	For consistency with similarly-sized metal furniture
* Replaced duct tape in mechanical parts recipe with oil
	Nuts, bolts, gears, washers, bearings... none of these require duct tape, but they may require coatings or lubrication
* Disabled recipe to melt snow at a campfire without a cooking pot (replaced with eating snowballs)
	If you don’t use the pot, you’re melting it in the jar, in which case there’s no reason you couldn’t boil it (and anything else) in the jar to get clean water.
* Added new recipe to turn 2 tires into a set of minibike wheels
	It fits better visually to require 2 tires, and this maintains the balance of total wheels available without affecting the amount of road debris

xui.html
XUi/windows.xml
* Added tools window to workbench, including the wrench, wire tool, and tool & die set
	As the workbench gains more recipes, it makes sense to use the existing tools mechanic to make more advanced things


Version 3.0	7/22/2017

* Merged all ComSenMod files with new Alpha 16 files
* Added .txt version of this Read Me file for server operators

Known Issues
* The flashlight makes no sound when you hit something with it, because the game can’t find an appropriate particle effect
* Plywood and other road debris sometimes floats above the ground
	It’s aligned to the bottom of its voxel and set as a decoration; that’s all the more that can be done as far as I know.  Cinder blocks have the same problem.

biomes.xml
* Adjusted biome temperatures to be a constant value colder than A16 vanilla’s temperature ranges
	A few biomes changed from A15, but the relative difference should stay the same
* Replaced whiteSidingWoodPanelBurnt7 with burntWoodBlock6
	Substitution for old block, which was removed

buffs.xml
* Slightly reduced warmth from campfires
	It’s seemed too extreme in testing, causing an annoying amount of overheating

blocks.xml
* restored 30% of the wood that dropped in Alpha 15 when destroying trees
	It’s an incentive to not leave half-destroyed trees around, and makes sense that some of the wood isn’t accessible until the whole tree comes down
* Adopted vanilla behavior of school desks dropping scrap plastic on destruction instead of on harvest
	The important part was for them to provide plastic
* Adopted vanilla value for scrap plastic dropped from destroyed blinds
	The important part was for them to provide plastic
* Adopted vanilla chance of harvesting mechanical parts from cars
	They were rebalanced to be more plentiful than A15, which was the original goal
* Changed old cabinet sink to use sink loot list instead of fridge loot list
	Assumed to be an oversight
* Re-implemented the non-centered plywood plate block
	For use as road decoration; looks & plays better than cinder block piles
* Added chance for intact and partially damaged cars to drop plastic when harvested
	Modern cars use lots of plastic
* Made hanging moss yield plant fibers when destroyed
	That’s what they’re made of, and it can save you a trip topside in the early game
* Changed bedroll’s repair and fall items to cotton
	To match its new recipe
* Changed material of bird nests from furniture to hay
	So that they’re weaker and make a more appropriate sound
* Reduced chance of planted trees dropping feathers by 25% (native trees are unchanged)
	To reduce the ability to ‘farm’ feathers in unlimited quantities
* Made burning barrels burn characters on top of them
	As you’d expect from a fire

entityclasses.xml
* Changed fat female zombie to use ‘fat zombies’ loot group
	She was using farmer loot, but she doesn’t look like a farmer
* Adopted vanilla experience points for killing dogs
	Wildlife, experience points, and enemy behavior have all changed a lot since A15, so rolling back this change

items.xml
* Reverted crossbow’s economic value to vanilla
	To reflect the crossbow’s demotion to a mid-game weapon
* Adopted vanilla value for gas can’s material
	“Fuel barrel” is more specific than plastic
* Adopted vanilla value for dynamite material
	Looks like it has its own dedicated material now
* Adopted vanilla value for running shoe weight
	The important part was for it to have a weight, so it can be scrapped
* Changed suit jacket material & repair material to cloth
	Same result as in vanilla, but necessary since it’s an extension of the jacket, which is now leather
* Adopted vanilla value for blood draw kit weight
	The important part was for it to have a weight, so it can be scrapped
* Adopted vanilla value for fertilizer material
	“Fertilized farmland” is more specific than organic
* Reading an armor book now increases “Clothing/Armor” skill
	Because light & heavy armor were merged into one new skill
* Reverted poncho repair material to leather
	It’s now treated as a leather poncho everywhere else
* Increased fullness & wellness from vegetable stew
	Compared to meat stew, it wasn’t high enough to justify the increased ingredients (5 potatoes, 5 corn, & 5 mushrooms)
* Reverted glue material from plastic back to organic
	Since you can turn bones into glue, you could in effect turn zombie corpses into plastic
* Increased fullness & wellness from blueberry pie
	For better consistency with other high-end foods, and to match its new recipe
* Made machetes harvest wood e.g. from trees, though with less yield than with an iron fireaxe
	A machete should still work in its original role as a wood-chopping tool

Localization - Quest.txt
* Updated basic survival quest numbering, all languages
	Because the order has changed
* Updated basic survival quest info, English version
	Because some recipes have changed
* Enclosed all basic survival quest descriptions in quotes, English version
	For better readability of the file
* Added instructions to first basic survival quest on how to equip an item, English version
	This important step wasn’t covered
* Added explanation to “start a base” description
	Without more instruction, it’s not clear why you need to build blocks, besides that the game tells you to.
* Removed references to negative insulation in the hot weather tip, English version
	The mod overhauls insulation to always be positive

materials.xml
* Enabled hay bales to be scrapped into plant fibers
	It’s logical, balanced, and you could do it before

recipes.xml
* Changed machete recipe to require a workbench & forged steel instead of iron
	To help distinguish the hunting knife as a mid-game weapon and the machete as a better, late-game weapon & tool
* Reverted torches to require tallow instead of animal fat
	As a roundabout way of requiring a fire to make more fire (render the fat in a campfire)
* Changed crucible recipe to require glass instead of mechanical parts
	A crucible has no moving parts, so mechanical parts didn’t work.  However some designs use clay with quartz sand, so glass is a closer analogue.  The quantities of stone and clay required still make it a late-game item.
* Increased blueberries & cornmeal required for blueberry pie
	For better consistency with other high-end foods, and to better reflect the abundance of different ingredients

loot.xml
* Reduced chance of finding repair kits in basic guns & ammo loot
	I was finding too many of them in testing
* Removed padlock from automotive loot
	Automobiles don’t have padlocks, and there was a lot of overlap with the tool group
* Reduced chance of finding night vision goggles in survival stash loot
	To reflect their increased usefulness since A15
* Rebalanced probabilities within backpack loot
	To match the A16 shift toward more whole firearms
* Increased max forged iron found on lumberjacks
	For consistency with other places forged iron is found
* Adjusted quantities of items in lab equipment loot
	For consistency with similar occurrences of the same items
* Made cooking pots a more likely find than cooking grills in oven loot
	Matching the relative frequency in A16 vanilla
* Added paint to sink loot
	It’s as or more plausible than finding it in a cupboard
* Adopted vanilla chance of finding guns in safe loot
	To match the A16 shift toward more whole firearms
* Reverted quantity of loot found on generic zombies to A15 levels
	The day-to-day quantity of zombie corpses to loot isn’t higher, and the mod provides more variety so there’s less duplicate loot
* Slightly increased chance of finding a firearm in cop loot
	To get closer to the vanilla A16 probability
* Adjusted quantities of cloth found in washing machine loot
	For consistency with other places cloth is found
* Set cop, nurse, wight, & business man zombies to use the new junkPersonal group instead of junk
	junkPersonal is more tailored to only include personal effects
* Removed paint tool from garage loot
	redundant with the tools group already part of this container
* Using dirty beverages in trash compactor loot instead of the old beverages
	Drinks found in trash aren’t reliably safe to drink
* Adjusted quantities of loot found in new shipping crates & collapsed stations
	For consistency with similar occurrences of the same items
* Added electronic parts to collapsed battery bank loot
	Representing broken, but salvageable parts
* Added gas cans, electric parts, & mechanical parts to collapsed generator bank loot
	Representing broken, but salvageable parts
* Restored zombie stripper’s use of its own loot list
	Assumed to be an oversight
* Created new weaponAllBows loot group and used it for ranged bandits, cowboy zombies, survival stashes, & ‘hero’ crates
	There was a hole where several zombies drop compound bows or their parts, but the other bows are absent in loot
* Added ladders to working stiffs & garage loot
	Ladders weren’t found in any loot, but they’re a very plausible find in these places, and useful for the early game
* Restored amount of loot found in pill cases to vanilla levels
	These aren’t the sealed crates I thought they were, and there was too much loot to find at a Pop ’n’ Pills
* Split chance of finding padlocks between desks & filing cabinets
	You might find a locked drawer in either, but rarely will it be a separate, non-integrated padlock
* Added facial piercings to zombie stripper loot
	She has a punk look that makes them seem appropriate, or they can represent her nipple rings
* Increased chances of zombie strippers carrying junk
	Now that this zombie spawns in the wild at any time, she should carry less rare loot
* Increased quantities of ammo when found together with the appropriate weapon
	To reduce the clutter of finding tiny amounts of different things, and to match the A16 shift toward more firearm use
* Adjusted chances of different loot from tree stumps
	Players were getting a bit too much good stuff in testing
* Increased the maximum number of eggs players could find at once by one
	Players were finding too few eggs in testing, and 3 eggs is still very plausible
* Removed gold & diamond from cupboard loot
	Only silver really makes sense, especially since cupboard loot is used elsewhere, like in coolers
* Added wood, duct tape, and plastic to skateboarder loot
	He was dropping too many mechanical parts, so these less valuable materials represent other parts of a skateboard
* Removed paint-related items from airdrop loot
	This was a consequence of using the Working Stiffs group in airdrops

quests.xml
* Re-ordered basic survival quest chain to: wooden club, stone axe, bow & arrows, start a base, bedroll, campfire, craft clothes, wear clothes, find trader
	Do the handheld items first and the clothes last, because in practice defending yourself from enemies is a shorter-term threat than freezing or overheating.  Make the club first, so that players have the simplest, single-ingredient recipe to follow when they’re first learning how to craft.  As for the bedroll, until you build or collect something, any place you could respawn is as good as every other place.  So start a base before putting down a bedroll, so there’s something to come back to.  Make the campfire next, to facilitate settling in one spot instead of just placing important things wherever.

weathersurvival.xml
* Let player get colder before they stop drying out (30 instead of 40) (reinstated from ComSenMod 2.0)
	Should be forgiving, because there’s a punishing feedback loop where you get cold because you’re wet and stay wet because you’re cold.  30 is closer to the freezing point.
* Lowered the maximum rate at which players can dry from 10% per second to 5% per second
	The above change makes the theoretical maximum higher, and this should reduce how often you have to swim to stay cool in hot weather

Version 2.5	5/10/2017

* Moved files to separate Config folder in the download for clarity and ease of installation

biomes.xml
* Reduced tires on roads by half
	Compensates for more spare tires found in cars
* Replaced cinder blocks on roads with other debris like hubcaps & driftwood
	Maintains the idea & visual interest of debris on the road with somewhat more plausible items

blocks.xml
* Changed material of purses from cloth to leather
	Purses are typically made of leather
* Changed material of bird nests from wood_weak to furniture
	wood_weak was too strong
* Set wooden desk to use new desk loot group
	to use the wooden drawer sounds without having to use nightstand loot
* Changed shopping basket material from metal to plastic
	They’re typically made of plastic
* Disabled fall damage on snow
	It’s soft like hay, and it gives a benefit to building in the snowy biome
* Marked new road debris blocks as terrain decorations
	This helps place them at ground level

entityclasses.xml
* Increased experience points for killing a dog by 25%
	Killing one dog requires the skill & effort of killing something like 2.5 regular zombies

items.xml
* Made empty buckets stackable up to 50
	More consistent with jars, pots, etc. now that buckets are found in loot
* Made stone arrows scrap to stone instead of wood
	The arrowhead is more durable than the shaft, so that’s the part that you’d salvage
* Changed material of bone & bone shiv from metal to wood
	For more bone-like sounds
* Changed material of torch from organic to wood
	For more wood-like sounds
* Changed blunderbuss ammo to scrap to stone instead of paper
	You would salvage the more durable part
* Changed gas can material from metal to plastic
	Probably inconsequential, but better matches UI icon
* Changed dynamite material from stone to dynamite
	There was already a dynamite material defined... oversight?
* Changed shopping basket material from metal to plastic
	They’re typically made of plastic
* Changed shopping basket to be repaired with plastic
	To match its new material
* Changed swat helmet from metal to military fiber
	“Military fiber” is used throughout the game for any high tech military-grade armor
* Changed swat helmet to be repaired with military fiber
	To match its new material
* Changed football & mining helmets from metal to plastic
	Research indicates they’ve been plastic since ~1950
* Changed football & mining helmets to be repaired with scrap plastic
	To match their new material
* Changed blood draw kit from metal to plastic
	Better matches the UI icon
* Added weight to blood draw kit
	So it can be scrapped
* Changed jackets from cloth to leather
	They look leather to me, especially the letterman version
* Changed coffee drink material from organic to glass
	For consistency with other drinks
* Changed fertilizer from metal to organic
	Assumed to be an oversight
* Changed glue from organic to plastic
	So that it scraps to something useful
* Reduced weight of glue
	To balance the amount of plastic from scrapping it
* Changed calipers from metal to brass
	To support new recipe
* Reading a book gives you a point in the related action skill
	Book learning isn’t worthless.  Reading a book about pistols should make you somewhat better with pistols, specifically, and not just with bullets & repair kits.  Books are still rare, so they supplement rather than supplant your need to fire thousands of bullets or get hit hundreds of times to become proficient.
* Changed flashlights, night vision goggles, & car batteries to be repaired with electrical parts instead of repair kits
	If it’s broken, the electrical parts are what would need repair.  Oil & duct tape won’t work.
* Changed animal hide clothing to be repaired with animal hide
	If you had leather, you probably wouldn’t need to be repairing your animal hide clothes in the first place
* Changed hunting knife & machete to be repaired with repair kits instead of forged iron
	A low durability blade probably needs sharpening rather than replacing, in which case a repair kit seems a closer analogue to an oilstone or strop
* Changed stone axe, stone shovel, & wooden bow to be repaired with plant fibers
	I figure the fiber would be the part that wears out fastest, and needs repairing most often
* Changed crossbow to be repaired with leather
	I figure the string would be the part that wears out fastest, and needs repairing most often
* Changed material & repair material for sunglasses & derivative eyewear from metal to plastic
	Plastic is most likely for the frames and the lenses, and repairing them with “broken” glass would feel weird
* Re-enabled repair properties for scrap plastic & electrical parts
	So that these work to repair items
* Raised block damage on machete to be as good on wood as an iron fire axe
	Machetes are specifically designed to chop wood, plus they’re rare and un-craftable in this game
* Increased economic value of crossbows by 50%
	To match the crossbow’s status as an endgame weapon (for now)

loot.xml
* Added padlock to locker loot
	Lockers often have locks. :)  Besides, padlocks were only found in 1 group.
* Added wood, plastic, iron, rotten food, beverages, & candy tin to locker loot
	Representing shelves & other scrappable items inside, and abandoned lunches
* Removed hats, paper, & gunpowder from locker loot
	Redundant with other groups already included
* Added quests & treasure maps to locker loot
	These follow naturally wherever books & paper are found
* Rebalanced probabilities of items found in locker loot
	Some things were so rare, you’d probably never find them
* Guaranteed Working Stiffs and other store-specific crates will have a minimum of 1 item
	No one would bother to package and seal a crate if it’s empty
* Reduced clothes found on generic zombies
	In playtesting I was finding too many clothes
* Reduced loot from cars back closer to vanilla
	In playtesting I was finding too much valuable loot, and duplicates
* Switched cars to use junkPersonal loot group instead of junk
	So you don’t find plant fibers, door knobs, etc.
* Added aloe cream to medicine loot
	Representing various first aid creams & ointments
* Made separate loot group for desks
	So that they don’t have clothes, while keeping the wooden drawer sounds
* Reduced chance of finding a crossbow on corpses
	I was finding them too often
* Added new “office supplies” group including paper, books, wood, iron, plastic, tape, glue, & electronic parts for desks & filing cabinets
	Representing things like pencils, pens, rulers, markers, staplers, calculators, etc.
* Replaced ammo in desks with pistol+ammo (still a rare find)
	A pistol seems more plausible than other weapons
* Reduced chance of finding pistol+ammo in toilets
	Finding it once is neat, but you would find too many over the course of a game
* Added vitamins to desks & filing cabinets
	Seems as likely to find as painkillers
* Increased quantities of glue you find at once
	To reduce the clutter of finding tiny amounts of different things
* Added extra chance for cop zombies to drop shades
	The classic cop look isn’t complete without these stylish aviators
* Adjusted air drops to drop fewer types of food at once
	For reduced clutter

quests.xml
* Reduced number of screamers & animals you need to kill for various challenges
	Difficulty aside, you could go many days before the game would spawn, say, 5 rabbits.  It was more luck than challenge.

recipes.xml
* Changed calipers recipe to require brass instead of steel
	Recipe was broken since steel isn’t a forge material
* Reordered flashlight recipe so it scraps to electrical parts
	You would salvage the more valuable part

weathersurvival.xml
* Reverted EnclosureDetectionThreshold, DryTempCutoff, DryPercentPerSecondPerDegree, CoreTempChangeRateWhenDry, CoreTempChangeRateWhenWet, BaseOutsideTempChangeWhenWet, OutsideTempChangeWhenInSunCloudScale back to vanilla values
	These changes either had no effect, the effects were poorly understood, or the problems they sought to fix weren’t adequately investigated.  I’ll stick to biome temperatures & insulation values until these variables are better understood and/or less buggy.

Version 2.0	3/31/2017

biomes.xml:
* Made all biomes 25 degrees cooler
	Compensates for what people would typically wear, now that clothing doesn’t cool the player

blocks.xml:
* Removed requirement to use a wrench when harvesting bird nests
	Wrenches look silly on organic things.  Now you can bust it up with an axe, like a tree.
* Changed desks to use file cabinet loot instead of dresser loot
	Clothes in a desk is uncommon; this loot list makes much more sense
* Changed material for school desks from furniture to metal
	So that it uses metal SFX & VFX, and the pickaxe works better than a fire axe on them
* Changed wall ovens to use oven loot instead of cupboard loot
	Assumed to be an oversight.  Cupboards are already abundant.

items.xml:
* Redesigned insulation of all items so that clothing & armor can only warm the player
	The system wasn’t robust enough to support warming and cooling items. No more taking off your shorts when you get cold.  More and heavier clothes = warmer, less and lighter clothes = cooler.
* Changed cigar material from cloth to plants, and added weight so it can be scrapped
	Cigars are rolled tobacco leaves, not cloth

loot.xml:
* Replaced coffee beans in sink loot with buckets
	This group is also used for public bathrooms, where coffee beans would be an odd find.
* Made all water murky, except when found in coolers, fridges, beer coolers, and shamway boxes
	In the age of a zombie infection, you can’t assume random water you find on a corpse is safe to drink
* Added water & canned food to air drop loot
	Complements that clean water is harder to come by.  Not sure why the airdropfood group wasn’t enabled.
* Added jackets wherever clothes or warm clothes are found
	Jackets were effectively disabled from the game.  They offer another tier of warmth.
* Removed medicine from stumps
	It didn’t feel right to find a beaker in there.  Stumps had enough different goodies as it is.
* Added goggles to warm clothes
	Ski goggles are cold weather gear, and they have a warming effect now
* Reduced amount of survival stash loot found in stumps
	I was finding too much good loot in the pine forest
* Increased quantities of arrowheads, while reducing the chance of finding them
	Incorporating feedback to reduce the clutter of finding a near-useless amount of something
* Increased minimum quantities of items in ammo & military ammo loot
	Incorporating feedback to reduce the clutter of finding a near-useless amount of something
* Removed duplicate entry for paper in locker loot
	Assumed to be an oversight
* Standardized quantities of paper found, outside of books & filing cabinets
	Incorporating feedback to reduce the clutter of finding a near-useless amount of something
* Removed rotten flesh from cold food loot
	Establishing a general convention that refrigerated food isn’t spoiled, while other food may be
* Removed some car parts from car loot & added other stuff you might find inside
	There might be a drink in the cup holder, a flashlight in the glove box, or motor oil in the trunk.  But if you want radiators, springs, and engines, you’ll have to harvest the car rather than loot it.
* Added snowballs to cold food loot
	Representing ice buildup on the wall of a cooler or freezer, which still has value to a thirsty survivor
* Increased minimum quantities of military fiber, potassium nitrate, oil, springs, cloth, gunpowder, scrap metals, wood, nails, casino tokens, bullet casings, feathers, grass, dirt, plastic, forged iron/steel, & leather found at once
	Incorporating feedback to reduce the clutter of finding a near-useless amount of something
* Removed old cash from junk loot
	People don’t just throw away money.  Still found on bodies.
* Increased amount of loot in fridges
	They were set to have less loot than coolers & shamway crates, despite being larger
* Added beverages to fridge loot
	More consistent with other food containers.  Refrigerating an empty jar is unusual, so now it will happen less often.
* Added books to backpack loot
	Books in a book bag?  What an idea! :)
* Replaced glass panes in junk with broken glass
	If it wasn’t broken, it probably wouldn’t be in the trash.  They were only good as forge material, anyway.
* Added cooking grill to oven loot & split probability of finding either
	The grill’s usefulness is already overshadowed by the pot.  It shouldn’t be overly rare, too.
* Added broken glass to medicine cabinet loot
	Represents ‘scrap glass’ from glass vials and broken mirrors.  Fits the game’s dilapidated look.
* Removed hazmat gear from regular zombies
	These clothes are too special case for any old zombie to have on them
* Slightly decreased chance to find mining helmet in cars
	Flashlights are more believable, and they appear more often now
* Added paper to cop & nurse loot
	For an air of authenticity: these jobs involve a lot of paperwork
* Added scrap brass to cop loot
	Representing their brass officer’s badge
* Reduced chance of finding flashlights in stumps & backpacks
	On further inspection, flashlights are meant to be rarer than I thought
* Cherry picked a few junk items for suitcases & rebalanced loot chances
	Suitcases are rare enough they don’t have to have common junk, much of which you wouldn’t find packed in a suitcase
* Added armor, crossbows, & old cash to corpse loot (the ones that are dead but not zombies)
	They needed more variety, so you don’t get too many magnum parts.  These items better ‘tell the story’ of this fallen survivor, plus crossbows weren’t found in any loot.
* Added candy tin to fat zombie loot & rescaled loot percentages
	Fat people like candy :)
* Added treasure maps & nerd glasses to filing cabinets
	The map makes shuffling through all those papers worthwhile, while the glasses are because the poindexter using the file cabinet is absentminded ;)
* Increased time to open suitcases, file cabinets, coffins, bookcases, dumpsters, and mortician’s drawers
	These are things that either take a moment to get open, or have lots of stuff inside to sort through
* Added trophies to football player loot
	If anyone should be carrying around a trophy, it should be these guys
* Created new “junkPersonal” loot list just for zombies & other bodies, with adjusted probabilities
	This way zombies don’t carry odd things like door knobs and candlesticks, but you can still find these in trash piles
* Added old cash and vitamins to junkPersonal loot
	People carry these things on them, and they’re no more valuable than the casino tokens and painkillers, respectively
* Added candles to junkPersonal loot
	Candles are thought of as lighters in this mod.  Giving them to zombies allows you to start a fire without relying on specific PoIs.
* Removed rotten food, quests, & treasure maps from generic zombie loot
	Now redundant with junkPersonal loot group
* Moved facial piercings from generic zombie loot to clothes loot
	These could be found, rarely, wherever clothes are found.  Individual zombie types have an extra chance of having them.
* Added junk to football player & utility worker loot
	For consistency with other UMA zombies
* Adjusted each zombie’s chance of dropping specific clothes
	On horde night you would get a glut of things like running shoes: more than you can even sell.
* Insured some type of clothing could be found on all corpses
	All zombies wear clothes (except ferals & animals), so it should be possible to loot clothes off of any of them.  Zombies drop generic clothes if no specific clothes are specified or, in the case of strippers, cloth fragments. :)
*	Took automotive loot out of air drop crates
	This was the one subset of working stiffs loot that didn’t fit well
* Added chrysanthemum seeds to seeds list
	If you can find other biome-specific seeds like aloe, you should find chrysanthemum, too

recipes.xml:
* Changed cornbread & blueberry pie recipes to use animal fat instead of water
	This is more true to life, and maintains the ‘water=pot’ convention.  These foods didn’t hydrate you, either.

weathersurvival.xml:
* Increased threshold before weather system considers you ‘inside’ from 15% enclosed to 25% enclosed
	Experimental - sounded too low, like it would almost always be in effect
* Decreased snowfall soak time from 5 minutes to 2 minutes
	Snow melts as soon as it hits skin, so IF you don’t have waterproof clothes, you should get soaked almost as fast as with rain.
* Let player get colder before they stop drying out (30 instead of 40)
	Should be forgiving, because there’s a punishing feedback loop where you get cold because you’re wet and stay wet because you’re cold.  30 is closer to the freezing point.
* Temperature has a less pronounced effect on how fast you dry out
	Lessens the feedback loop, and re-scales the curve to fit the above change
* Narrowed the difference in how fast player changes temperature when wet versus dry
	It looks like this affects how fast you cool down AND heat up.  You shouldn’t heat up faster when wet, so this is a compromise.
* Expanded range of temperatures under which you heat up/cool down at regular speed
	If you’re not hot or cold, you don’t really need to warm up or cool down extra fast
* Reduced temperature drop when wet from 30 to 20 degrees
	This is very hard to model accurately without humidity, so wind will be a bigger factor as an approximation 
* Disabled BaseOutsideTempChangeWhenWet
	Research indicates this is an absolute value that negated biome conditions.
* Increased the cooling effect of the wind
	Wind plays a bigger role in absence of other factors like humidity.  Now wet skin can ‘feel’ twice as cold when it’s windy.
* Made a cloudy sky only warm you 20% as much as a sunny sky
	I researched what a good value would be, but in the end just went with what felt intuitive.
* Increased temperature shift when running to 10 degrees
	Running never had an appreciable effect on temperature.
* Remapped elevation’s effect on temperature to a parabolic curve once above ground
	This way you only really notice it getting cold as you get up ‘in the mountains.’  Less realistic, but remember we’re compressing thousands of real meters into 250 game meters.

Version 1.0	2/23/2017


biomes.xml:
* Reduced max surface rock probability (found in clay subbiomes) from .025 to .015
	Aesthetically, the 2 rock models used are old Unity assets that look bad when repeated so often on screen
	Balance-wise, these were so abundant, you never needed to mine underground
* Quadrupled chance of mining silver/gold/diamond ore in all biomes
	Don’t have a feature so rare the player never encounters it.  That’s still a 1 in 1250 chance to hit silver, just among sub-biome blocks, and the other ores are rarer.
* Reduced hollow tree stumps by 50%
	There shouldn’t be many of them within eyesight.  It’s visually repetitious, and too many warm clothes growing on trees nullifies the unique challenges of the snowy biome.
* Reduced bird nests by 50%
	Goes with another change to put ‘bird nests’ in trees, where players intuitively expect to find them
* Reduced snowberries in forest subbiome by 50%
	They were unnaturally thick, and more abundant in temperate forest clay than any other place

blocks.xml:
* Moved harvesting car headlights from fully damaged state to somewhat damaged state
	The headlight is only visible in the intact and somewhat-damaged models.  Besides, it would be broken long before the car is down to its metal chassis.
* Added chance to harvest car batteries from undamaged cars
	Logically, car batteries are easily accessible and removable without having to strip down the car first.
	Balance-wise, players weren’t harvesting enough batteries relative to the number of headlights.
* Any tree with harvestable wood has a chance to drop feathers when destroyed.  Trees that also bear seeds have a 50% greater chance of feathers.
	Most birds make nests in trees, so players intuitively expect to find them there.  This represents picking through any bird nests that may be in the tree after it falls, while the eggs break from the fall.
* Doubled chance of harvesting mechanical parts from all stages of cars
	A car has far more bolts, gears, etc. than other sources of mechanical parts, like chairs and toilets
* Changed coffins to use their own loot list
	Coffins should have clothes & bones over random junk
* House front doors have a chance to drop doorknobs when destroyed
	The doorknob is clearly visible, and this is consistent with other brass fixtures in these houses
* Bird nests drop wood when destroyed instead of plant fibers
	The nest’s material is set to wood.  When you hit it, it sounds like wood, and makes wood particles.
* School desks can be harvested for scrap plastic & iron
	The seat and desktop are made of plastic.  It was probably set up before plastics & harvesting were introduced
* Cacti drop wood when destroyed instead of yucca fruit
	Cacti were effectively just another yucca plant, and too much fruit makes hunger & thirst a nonissue.  Now players will still appreciate the wood, from which the ribs of a real saguaro are made.
* Blinds drop scrap plastic when destroyed
	These were probably created before the game had plastic as a material

buffs.xml:
* Increased splint effectiveness from 2x healing speed to 3x
	The healing time was still frustratingly slow when you consider a splint is the only and best remedy a player has, and how easily legs sprain and break.

entityclasses.xml
* Set basic female zombies to drop basic zombie loot instead of fat zombie loot
	This is expected to lower the overall amount of food from zombies considerably.  It was probably an oversight.

items.xml:
* Increased chance of torches alighting enemies from 10% to 25%
	This is the one obvious thing players expect could happen when hitting a zombie with a torch.  Torches aren’t trivial to make and are poor weapons otherwise; this helps the game ‘look right’ more than anything.
* added weight to running shoes so they can be scrapped
	No reason these shouldn’t be scrappable like all other shoes.  Probably an oversight.

loot.xml:
* Added small chance to find precious metals in cupboards & drawers
	This represents finding fine silverware.
* Increased quantities found for some stackable junk loot, like nails
	Finding one nail at a time is useless; it just takes up inventory space.  Finding a handful of nails is at least equally plausible and more likely to be good for something other than scrap.
* Added scrap iron to junk
	Representing all the random stuff people throw away containing iron or other cheap metals 
* Added clothes to junk
	Old clothes get thrown away.  Naked in the apocalypse, you’d be happy to wear dirty rags.
* Added plant fibers & dirt fragments to junk
	Representing yard waste & decomposing matter, and that junk tends to be dirty. :)
* Made first aid kits twice as common as other rare medicine
	They’re less valuable than beakers, antibiotics, blood draw kits, and first aid schematics, so they should appear more often.
* Added medicine to lootable backpacks
	Medicine’s just a sensible thing someone traveling with a backpack would pack.
* Renormalized backpack loot probabilities
	No effect on gameplay, just easier to compute at a glance
* Added scrap plastic to medicine & sinks
	Representing old plastic bottles one would find under sinks and wherever medicine is found (mostly medicine cabinets)
* Increased probability of old cash from safes
	Safes are where the money is. :)
* Added iron club to zombie cop loot
	Representing a billy club
* Added tools to garage loot
	What garage doesn’t have some tools lying around?
* Added working stiffs loot to airdrops (including chance to spawn rare tools like calipers)
	The army is enlightened enough to realize you don’t just need stuff, you need things for making stuff.  Teach a man to fish and all that.
* Added eggs, feathers, and mushrooms to hollow stumps
	Representing that dead stumps may be home to nesting birds and growing fungus
* Added clothes and books to suitcases
	What do people pack in suitcases?  Clothes, mostly.  Maybe a book to read.  This isn’t rocket science. :p
* Replaced instances of Sham sandwiches in loot with all types of rotten food
	A sandwich contains meat and bread.  But since you can’t scrap a sandwich to get either of these (material=“organic”), zombies should drop the pieces sometimes instead of the whole sandwich.
* Added repair kit to guns+ammo loot group
	It makes sense people would keep materials for repairing/maintaining their guns with their guns and ammo.
* Added goldenrod & red tea to beverage loot
	No reason not to add these: they’re drinks you’d find in coolers where this loot group occurs, and their value lies between beer and water
* Reduced container size for purse and bird nest from 12 to 8
	These container’s capacities didn’t reflect their small physical size.  8 is small enough to notice, without being too small for the loot they might contain.  
* Increased max number of casino tokens from cash registers by 50%
	I found that I never got enough tokens from a store to be able to buy something from its vending machine, which makes the convenience of having vending machines in different stores irrelevant.
* Split backpack loot between ‘cupboard’ food and rotten food
	This reflects that some people packed perishable food in their backpacks, which are often moldy and decomposing by now.
* Doubled max amount of loot in dumpsters
	Dumpsters are big.  Their container grids are large, but they only spawned as much loot as a small trash pile.  It’s still junk, there’s just more of it.
* Increased Utility Worker’s chance of dropping tools
	If there’s one zombie you’d expect to be carrying a hammer, wrench, or other tools, it’s this guy.
* Added a number of Working Stiffs-type loot to Utility/Construction Worker zombie loot
	Same.  This changes the zombie from merely looking different into a sought-after target.
* Removed books from Mortician’s Drawer
	Why would there ever be a book in there?
* Added facial piercings to skateboarder zombie loot
	It fits the skateboarder stereotype.
* Added facial piercings & black bandana to biker zombie loot
	It fits the biker stereotype.
* Replaced beer with grain alcohol in farmer zombie loot
	Anyone can drink beer.  Homegrown moonshine has more backwoods charm. :)
* Added overalls to farmer zombie loot
	It fits the farmer stereotype.
* Moved trophies out of filing cabinets and into safes
	Keeping a trophy in a safe seems much more plausible than keeping it in a filing cabinet.  Who does that?
* Slightly increased possible feathers & eggs per bird nest
	Offsets lower nest frequency
* Added rare medicine to Pop n Pills loot
	If a football player can drop a first aid kit schematic or a beaker, surely you should be able to find them at a pharmacy.
* Reduced amount of medicine you can get from airdrops
	On the default 3 days between airdrops, you accumulate too many antibiotics and beakers
* Doubled amount of loot you can find in cars
	Cars are larger than other containers.  They have more grid space and they occupy many blocks, so it makes sense that, like dumpsters, they can hold more things.
* Increased max forged iron or steel you can find from several containers from 2 to 10
	You can’t do anything with 2 forged iron/steel, and they’re too rare to accumulate enough from multiple sources to do anything.  I assume this is a holdover from when it took less iron to make things.
* Reduced container size of gas pump from 32 to 20
	Only gas spawns in gas pumps; there’s no need for extra space
* Made new loot list for coffins
	Coffins should have bones & clothes over random junk
* Standardized sources of scrap plastic, other than UMA zombies, to spawn 1-8 units
	You can’t do hardly anything with 3 units of plastic
* Added bucket to tools loot group
	Buckets weren’t found in any loot.  This puts them alongside other common hardware.
* Added military armor & hazmat gear to airdrop loot
	If they’re willing to give you military weapons, they should be willing to give you military armor.
* Transferred hazmat gear from lumberjacks to nurses & doubled probability to 0.02
	One would sooner expect a nurse to encounter hazardous materials than a lumberjack.
* Added scrap armor to heavy armor loot group
	Scrap armor wasn’t found in any loot.  This makes them appear rarely in backpacks.
* Added concrete mix to working stiffs loot
	You’d find it in a hardware store and, like rebar, it’ll give a player a nice timesaving, versatile leg up on building.
* Added a rare chance to find seeds and duct tape in mailboxes
	Trying to make mailboxes less boring by adding better things to rarely find.  Also, these items weren’t found in many different places.  Duct tape represents packing tape & other adhesives you could reuse.
* Reduced amount of oil you find in junk
	Now it matches the amount you find in the automotive loot group
* Switched garbage piles & dumpsters to use new “trash” quality template
	Junk now contains items with quality levels, which should be low quality since they’re junk
* Loot found in trash (pile, dumpster, can) has lower quality by using a new quality template
	This became necessary now that clothes, which have a quality, are found in trash
* Removed duplicate entry for coffee beans in seed loot group
	Assumed to be an oversight
* Added black shades, worn boots to warm clothes loot group
	Where there are shades, there should be black shades.  Boots are warm.
* Adjusted probabilities of individual ammo types in ammo loot group
	They were all equal except for magnum rounds.  They now better reflect the scarcity/power/skill level of each type and/or the weapons that use them.
* Made new “survival stash” loot group to replace sporting goods
	Found only in tree stumps, many sporting goods weren’t relevant.  Now it’s stuff someone would stash on a hunting trip.
* Reduced chance of finding doorknobs in junk by half
	Doors now sometimes drop doorknobs when destroyed, so this is to keep the overall balance of brass roughly the same

quests.xml:
* Updated bedroll quest to match new recipe
* Updated campfire quest to match new recipe

recipes.xml:
* Changed bedroll recipe to require cloth & cotton
	A bed is valuable for gameplay and imparts a degree of permanence.  It should take more than 5 seconds worth of effort to make one.  Helps justify very abundant cotton plants, and could deter PvP griefers.
* Added calipers recipe requiring tool & die set
	Addresses the odd situation of finding the tool & die set before you find calipers, which means you can make rockets before you can make bullets.  Tool & die sets are for making tools, so it works.
* Added alternative steel arrow & steel bolt recipes using plastic and a workbench instead of feathers
	This pairs with more abundant scrap plastic.  Players can use more ‘high-tech’ plastic fletching to complement more ‘high-tech’ steel arrowheads.
* Changed exploding crossbow bolt recipe to use scrap plastic instead of feathers
	This pairs with more abundant scrap plastic, and reflects the higher-tech nature of these ammunitions.
* Reduced electric parts needed for flashlight to not exceed other craftable lights
	Flashlights are smaller and less complex than wall lights, so they shouldn’t require more electric parts.
* Added candle/torch to campfire recipe
	You can’t make a fire with just rocks.  You need a source of ignition.  This changes the early game radically, but is pivotal for this to really be considered a survival game.
* Reduced smelting time for brick blocks by about one third
	The long forging times are a side effect of bricks being all clay.  In short, when you compare the hit points of various materials as a function of the time to make them, brick was not competitive.
* Changed food recipes that don’t use water to require the grill instead of the pot
	The grill was underutilized.  There was almost no reason to get one.  Now both the pot and the grill offer a number of food options.
* Changed blunderbuss recipe to use brass instead of forged iron (doesn’t require forge)
	By the time most players could make a blunderbuss, they’d moved on to better weapons, so the blunderbuss didn’t fill any role.
* Added alternate mining helmet recipe that uses ZU football helmet
	The ZU football helmet is just a different color; it should work the same
