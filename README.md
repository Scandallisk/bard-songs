# Legends of Aria bard-songs feature
Expand the song library on your server with SCAN's custom bard songs.

This feature gives players additional song choices in their Bard Songbook by expanding the options with three more songs.

- These bard songs are designed to improve the gameplay experience of groups & parties.
- These songs are automatically learned by a player and requires no recipies or training.
- Custom animations have been added to each song to make sure the player can see and recognize each song's special effect.

#### Produced by SCAN & from HOPE Society

## Instructions

- Simply copy paste the code below into the file names listed at the specific line.  
- You will be required to restart your server for these changes to take effect.  
- If you make changes while other players are on your server you will risk crashing your server and forcing a restart.  

To protect our community, please schedule downtime before deploying this change.

This code was produced for PublicServer version 1.4.7




# Files requiring an update

## barding.lua

    Lines 122-159

Path:  base > scripts > globals > static_data > prestige > barding.lua

### Song of Iron
#### Skill Level Requirement = 75
#### Descripton - Increase party defense by +10.


        --SCAN ADDED
        SongOfIron = {
            NoTrainingRequired = true,
            NeedSongBook = true,
            --NeedLOS = true,
            AbilityType = "Song",
            
            Action = {
                DisplayName = "Song of Iron",
                Icon = "Holy Shield",
                Enabled = true
            },
            NoCombat = true,
            NoResetSwing = true,
            Prerequisites = {},
            Tooltip = "Provides defense to nearby allies.",
            RequiresInstrument = true, -- Does this song require an instrument?
            RequiresResource = { Mana = 10 },
            MobileEffect = "SongAOE",
            Rank = 7,
            MobileEffectArgs = {
                SkillRequirement = 75, -- music/entertaining skill required
                PulseDuration = 5,
                MaxPulseCount = 3,
                MobileMod = "DefensePlus",
                MobileModID = "SongOfIron",
                MobileModAmount = 10,
                AreaOfEffect = 15,
                BuffIcon = "Holy Shield",
                BuffDescription = "Increase party defense by +10.",
                FriendOnly = true,
                BardEffect = "MusicNoteIntensity2Effect",
                TargetEffect = "VanguardEffect",
                SongSFX = "event:/magic/bard/song_of_water",
            },
            Cooldown = TimeSpan.FromSeconds(15),
            CastTime = TimeSpan.FromSeconds(1.5),
        },
        
        

## barding.lua

    Lines 161-198

Path:  base > scripts > globals > static_data > prestige > barding.lua

### Song of Wind

#### Skill Level Requirement = 40

#### Descripton - Increase party movement speed by 20%.


        --SCAN ADDED
        SongOfWind = {
            NoTrainingRequired = true,
            NeedSongBook = true,
            --NeedLOS = true,
            AbilityType = "Song",
            
            Action = {
                DisplayName = "Song of Wind",
                Icon = "Tracking",
                Enabled = true
            },
            NoCombat = true,
            NoResetSwing = true,
            Prerequisites = {},
            Tooltip = "Provides increased movement speed to nearby allies.",
            RequiresInstrument = true, -- Does this song require an instrument?
            RequiresResource = { Mana = 10 },
            MobileEffect = "SongAOE",
            Rank = 4,
            MobileEffectArgs = {
                SkillRequirement = 40, -- music/entertaining skill required
                PulseDuration = 5,
                MaxPulseCount = 3,
                MobileMod = "MoveSpeedPlus",
                MobileModID = "SongOfWind",
                MobileModAmount = .20,
                AreaOfEffect = 20,
                BuffIcon = "Tracking",
                BuffDescription = "Increase party movement speed by 20%",
                FriendOnly = true,
                BardEffect = "MusicNoteIntensity2Effect",
                TargetEffect = "PrimedAir",
                SongSFX = "event:/magic/bard/song_of_thew",
            },
            Cooldown = TimeSpan.FromSeconds(15),
            CastTime = TimeSpan.FromSeconds(1.5),
        },
        
        

## barding.lua

    Lines 201-237

Path:  base > scripts > globals > static_data > prestige > barding.lua

### Song of Rage

#### Skill Level Requirement = 60

#### Descripton - Increase party Bloodlust regeneration by +2 per second.


        --SCAN ADDED
        SongOfRage = {
            NoTrainingRequired = true,
            NeedSongBook = true,
            --NeedLOS = true,
            AbilityType = "Song",
            
            Action = {
                DisplayName = "Song of Rage",
                Icon = "Berserker Rage",
                Enabled = true
            },
            NoCombat = true,
            NoResetSwing = true,
            Prerequisites = {},
            Tooltip = "Provides Bloodlust regeneration to nearby allies.",
            RequiresInstrument = true, -- Does this song require an instrument?
            RequiresResource = { Mana = 10 },
            MobileEffect = "SongAOE",
            Rank = 6,
            MobileEffectArgs = {
                SkillRequirement = 60, -- music/entertaining skill required
                PulseDuration = 1,
                MaxPulseCount = 15,
                MobileMod = "BloodlustRegenPlus",
                MobileModID = "SongOfRage",
                MobileModAmount = 2,
                AreaOfEffect = 15,
                BuffIcon = "Berserker Rage",
                BuffDescription = "Increase party bloodlust regeneration by +2 per second.",
                FriendOnly = true,
                BardEffect = "MusicNoteIntensity2Effect",
                TargetEffect = "WarriorDemoStatus",
                SongSFX = "event:/magic/bard/song_of_earth",
            },
            Cooldown = TimeSpan.FromSeconds(15),
            CastTime = TimeSpan.FromSeconds(1.5),
        },
        
