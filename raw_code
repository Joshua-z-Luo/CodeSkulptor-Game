#######################################################################################################################################################################################################################################################################################################################################
#2d platfrom shooter. Written By Joshua Luo
#Inspired by Escape From Tarkov and Castle Crashers

import simplegui, random

# Load image
#player_image 
player_image = {'death_right':simplegui.load_image("https://i.imgur.com/e0Qx7oT.png"),
                'death_left':simplegui.load_image("https://i.imgur.com/R9lWrxW.png"),
                'shoot_right':simplegui.load_image("https://i.imgur.com/M8jTjiR.png"), 
                'shoot_left':simplegui.load_image("https://i.imgur.com/bDu1ScZ.png"), 
                'walk_right':simplegui.load_image("https://i.imgur.com/kuVPQJR.png"),
                'walk_left':simplegui.load_image("https://i.imgur.com/QdlmCR4.png"),
                'roll_right':simplegui.load_image("https://i.imgur.com/HSDcjQQ.png"),
                'roll_left':simplegui.load_image("https://i.imgur.com/u1j61MS.png"),
                'reload_right':simplegui.load_image("https://i.imgur.com/asm5ITK.png"),
                'reload_left':simplegui.load_image("https://i.imgur.com/LSoQQxh.png"),
                'check_right':simplegui.load_image("https://i.imgur.com/0GyaULs.png"),
                'check_left':simplegui.load_image("https://i.imgur.com/tFG1P6o.png")}

#player dimensions stuffs
# Size of image files 
PLAYER_COLS = {'death_right':15,
        'death_left':15,
        'shoot_right':2,
        'shoot_left':2,
        'walk_right':4,
        'walk_left':4,
        'roll_right':4,
        'roll_left':4,
        'reload_right':8,
        'reload_left':8,
        'check_right':5,
        'check_left':5}

PLAYER_ROWS = {'death_right':2,
        'death_left':2,
        'shoot_right':1,
        'shoot_left':1,
        'walk_right':2,
        'walk_left':2,
        'roll_right':2,
        'roll_left':2,
        'reload_right':2,
        'reload_left':2,
        'check_right':2,
        'check_left':2}

# Use width and height of as single cell in
# the sprite sheet
PLAYER_IMG_WIDTH = {'death_right':3840/PLAYER_COLS['death_right'],
                    'death_left':3840/PLAYER_COLS['death_left'],
                     'shoot_right':512/PLAYER_COLS['shoot_right'],
                     'shoot_left':512/PLAYER_COLS['shoot_left'],
                     'walk_right':1024/PLAYER_COLS['walk_right'],
                     'walk_left':1024/PLAYER_COLS['walk_left'],
                     'roll_right':1024/PLAYER_COLS['roll_right'],
                     'roll_left':1024/PLAYER_COLS['roll_left'],
                     'reload_right':2048/PLAYER_COLS['reload_right'],
                     'reload_left':2048/PLAYER_COLS['reload_left'],
                     'check_right':1280/PLAYER_COLS['check_right'],
                     'check_left':1280/PLAYER_COLS['check_left']}

PLAYER_IMG_HEIGHT = {'death_right':512/PLAYER_ROWS['death_right'],
                      'death_left':512/PLAYER_ROWS['death_left'],
                      'shoot_right':256/PLAYER_ROWS['shoot_right'],
                      'shoot_left':256/PLAYER_ROWS['shoot_left'],
                      'walk_right':512/PLAYER_ROWS['walk_right'],
                      'walk_left':512/PLAYER_ROWS['walk_left'],
                      'roll_right':512/PLAYER_ROWS['roll_right'],
                      'roll_left':512/PLAYER_ROWS['roll_left'],
                      'reload_right':512/PLAYER_ROWS['reload_right'],
                      'reload_left':512/PLAYER_ROWS['reload_left'],
                      'check_right':512/PLAYER_ROWS['check_right'],
                      'check_left':512/PLAYER_ROWS['check_left']}

reshala_image = {'walk_right':simplegui.load_image("https://i.imgur.com/5wDGsHL.png"),
                'walk_left':simplegui.load_image("https://i.imgur.com/bRXYZXo.png")}

#guard dimensions stuffs
# Size of image files 
RESHALA_COLS = {'walk_right':1,
        'walk_left':1}

RESHALA_ROWS = {'walk_right':1,
        'walk_left':1}

# Use width and height of as single cell in
# the sprite sheet
RESHALA_IMG_WIDTH = {'walk_right':256/RESHALA_COLS['walk_right'],
                     'walk_left':256/RESHALA_COLS['walk_left']}

RESHALA_IMG_HEIGHT = {'walk_right':256/RESHALA_ROWS['walk_right'],
                      'walk_left':256/RESHALA_ROWS['walk_left']}

guard_image = {'death_right':simplegui.load_image("https://i.imgur.com/0CA3jXR.png"),
                'death_left':simplegui.load_image("https://i.imgur.com/uVVbpPq.png"),
                'shoot_right':simplegui.load_image("https://i.imgur.com/Xj0uZ8F.png"), 
                'shoot_left':simplegui.load_image("https://i.imgur.com/hzoPleK.png"), 
                'walk_right':simplegui.load_image("https://i.imgur.com/VyEEENv.png"),
                'walk_left':simplegui.load_image("https://i.imgur.com/tF2EimL.png")}

#guard dimensions stuffs
# Size of image files 
GUARD_COLS = {'death_right':15,
        'death_left':15,
        'shoot_right':2,
        'shoot_left':2,
        'walk_right':4,
        'walk_left':4}

GUARD_ROWS = {'death_right':2,
        'death_left':2,
        'shoot_right':1,
        'shoot_left':1,
        'walk_right':2,
        'walk_left':2}

# Use width and height of as single cell in
# the sprite sheet
GUARD_IMG_WIDTH = {'death_right':3840/GUARD_COLS['death_right'],
                    'death_left':3840/GUARD_COLS['death_left'],
                     'shoot_right':512/GUARD_COLS['shoot_right'],
                     'shoot_left':512/GUARD_COLS['shoot_left'],
                     'walk_right':1024/GUARD_COLS['walk_right'],
                     'walk_left':1024/GUARD_COLS['walk_left']}

GUARD_IMG_HEIGHT = {'death_right':512/GUARD_ROWS['death_right'],
                      'death_left':512/GUARD_ROWS['death_left'],
                      'shoot_right':256/GUARD_ROWS['shoot_right'],
                      'shoot_left':256/GUARD_ROWS['shoot_left'],
                      'walk_right':512/GUARD_ROWS['walk_right'],
                      'walk_left':512/GUARD_ROWS['walk_left']}

#bot images
#assault things ##############
assault_image = {'idle':simplegui.load_image("https://i.imgur.com/PAVZMcU.png"),
                'shoot_right':simplegui.load_image("https://i.imgur.com/I16fLyi.png"), 
                'shoot_left':simplegui.load_image("https://i.imgur.com/fDnulP7.png"), 
                'walk_right':simplegui.load_image("https://i.imgur.com/DPed9M8.png"),
                'walk_left':simplegui.load_image("https://i.imgur.com/UfN2v61.png"),
                'death_right':simplegui.load_image("https://i.imgur.com/BuQ14et.png"),
                'death_left':simplegui.load_image("https://i.imgur.com/pbLzU24.png")}

ASSAULT_COLS = {'death_right':10,
        'death_left':10,
        'idle':23,
        'shoot_right':4,
        'shoot_left':4,
        'walk_right':4,
        'walk_left':4}

ASSAULT_ROWS = {'death_right':2,
        'death_left':2,
        'idle':2,
        'shoot_right':2,
        'shoot_left':2,
        'walk_right':2,
        'walk_left':2}

ASSAULT_IMG_WIDTH = {'death_right':2560/ASSAULT_COLS['death_right'],
                     'death_left':2560/ASSAULT_COLS['death_left'],
                     'shoot_right':1024/ASSAULT_COLS['shoot_right'],
                     'shoot_left':1024/ASSAULT_COLS['shoot_left'],
                     'walk_right':1024/ASSAULT_COLS['walk_right'],
                     'walk_left':1024/ASSAULT_COLS['walk_left']}

ASSAULT_IMG_HEIGHT = {'death_right':512/ASSAULT_ROWS['death_right'],
                      'death_left':512/ASSAULT_ROWS['death_left'],
                      'shoot_right':512/ASSAULT_ROWS['shoot_right'],
                      'shoot_left':512/ASSAULT_ROWS['shoot_left'],
                      'walk_right':512/ASSAULT_ROWS['walk_right'],
                      'walk_left':512/ASSAULT_ROWS['walk_left']}


#Defender things ####################

defender_image = {'shoot_right':simplegui.load_image("https://i.imgur.com/7qWDdeL.png"), 
                'shoot_left':simplegui.load_image("https://i.imgur.com/1JJgJLB.png"), 
                'walk_right':simplegui.load_image("https://i.imgur.com/9bXjiu6.png"),
                'walk_left':simplegui.load_image("https://i.imgur.com/hea670F.png"),
                'death_right':simplegui.load_image("https://i.imgur.com/j3B9nbw.png"),
                'death_left':simplegui.load_image("https://i.imgur.com/7vVrWTi.png")}


DEFENDER_COLS = {'death_right':10,
        'death_left':10,
        'shoot_right':4,
        'shoot_left':4,
        'walk_right':4,
        'walk_left':4}

DEFENDER_ROWS = {'death_right':2,
        'death_left':2,
        'shoot_right':2,
        'shoot_left':2,
        'walk_right':2,
        'walk_left':2}


DEFENDER_IMG_WIDTH = {'death_right':2560/DEFENDER_COLS['death_right'],
                     'death_left':2560/DEFENDER_COLS['death_left'],
                     'shoot_right':1024/DEFENDER_COLS['shoot_right'],
                     'shoot_left':1024/DEFENDER_COLS['shoot_left'],
                     'walk_right':1024/DEFENDER_COLS['walk_right'],
                     'walk_left':1024/DEFENDER_COLS['walk_left']}

DEFENDER_IMG_HEIGHT = {'death_right':512/DEFENDER_ROWS['death_right'],
                      'death_left':512/DEFENDER_ROWS['death_left'],
                      'shoot_right':512/DEFENDER_ROWS['shoot_right'],
                      'shoot_left':512/DEFENDER_ROWS['shoot_left'],
                      'walk_right':512/DEFENDER_ROWS['walk_right'],
                      'walk_left':512/DEFENDER_ROWS['walk_left']}


#Scout Things ##########
scout_image = {'shoot_right':simplegui.load_image("https://i.imgur.com/E0rjEQH.png"), 
                'shoot_left':simplegui.load_image("https://i.imgur.com/pU882XE.png"), 
                'walk_right':simplegui.load_image("https://i.imgur.com/DDsPSg5.png"),
                'walk_left':simplegui.load_image("https://i.imgur.com/nrJUdkr.png"),
                'death_right':simplegui.load_image("https://i.imgur.com/Br4Ef4I.png"),
                'death_left':simplegui.load_image("https://i.imgur.com/66y00i9.png")}

SCOUT_COLS = {'death_right':13,
        'death_left':13,
        'shoot_right':5,
        'shoot_left':5,
        'walk_right':4,
        'walk_left':4}

SCOUT_ROWS = {'death_right':2,
        'death_left':2,
        'shoot_right':1,
        'shoot_left':1,
        'walk_right':2,
        'walk_left':2}


SCOUT_IMG_WIDTH = {'death_right':3328 /SCOUT_COLS['death_right'],
                     'death_left':3328 /SCOUT_COLS['death_left'],
                     'shoot_right':1280/SCOUT_COLS['shoot_right'],
                     'shoot_left':1280/SCOUT_COLS['shoot_left'],
                     'walk_right':1024/SCOUT_COLS['walk_right'],
                     'walk_left':1024/SCOUT_COLS['walk_left']}

SCOUT_IMG_HEIGHT = {'death_right':512/SCOUT_ROWS['death_right'],
                      'death_left':512/SCOUT_ROWS['death_left'],
                      'shoot_right':256/SCOUT_ROWS['shoot_right'],
                      'shoot_left':256/SCOUT_ROWS['shoot_left'],
                      'walk_right':512/SCOUT_ROWS['walk_right'],
                      'walk_left':512/SCOUT_ROWS['walk_left']}

#bullet image
bullet_image = simplegui.load_image("https://i.imgur.com/7LmBEIw.png")


#background images
bgrd_image = [simplegui.load_image("https://i.imgur.com/Dr38BkH.png"),
              simplegui.load_image("https://i.imgur.com/X4XT9mb.png"),
              simplegui.load_image("https://i.imgur.com/LaaXEWM.png"),
              simplegui.load_image("https://i.imgur.com/YEygkuS.png"),
              simplegui.load_image("https://i.imgur.com/KE5OkAs.png")]

#blood images
blood_image = {'blood_right':simplegui.load_image("https://i.imgur.com/fYZSqhB.png"),
                'blood_left':simplegui.load_image("https://i.imgur.com/7Q3UaHM.png"),}



#number image
number_image = simplegui.load_image("https://i.imgur.com/WAPqGJ6.png")

#menu image
menu_image = simplegui.load_image("https://i.imgur.com/F9JEqU8.png")

#bullet image attributes
BULLET_IMG_WIDTH = 64
BULLET_IMG_HEIGHT = 64

BULLET_SIZE = (64,64)

BLOOD_SIZE = (256, 256)

NUMBER_SIZE = (24, 40)
NUMBER_COLS = 5
NUMBER_ROWS = 2

NUMBER_IMG_WIDTH = 24
NUMBER_IMG_HEIGHT = 40

BLOOD_COLS = {'blood_right':2,
        'blood_left':2}


BLOOD_ROWS = {'blood_right':2,
        'blood_left':2}


BLOOD_IMG_WIDTH = {'blood_right':512/BLOOD_COLS['blood_right'],
                    'blood_left':512/BLOOD_COLS['blood_left']}

BLOOD_IMG_HEIGHT = {'blood_right':512/BLOOD_ROWS['blood_right'],
                      'blood_left':512/BLOOD_ROWS['blood_left']}

bleedoverlay_image = simplegui.load_image("https://i.imgur.com/GtavJvI.png")

BLEEDOVERLAY_COLS = 5
BLEEDOVERLAY_ROWS = 2

BLEEDOVERLAY_IMG_WIDTH = 1920
BLEEDOVERLAY_IMG_HEIGHT = 980

credit_image = simplegui.load_image("https://i.imgur.com/NZJOfkb.png")

CREDIT_COLS = 5
CREDIT_ROWS = 2

CREDIT_IMG_WIDTH = 1920
CREDIT_IMG_HEIGHT = 980

while bleedoverlay_image.get_width() == 0:
    pass

death_image = simplegui.load_image("https://i.imgur.com/nYDxbkW.png")

DEATH_IMG_WIDTH = 1920
DEATH_IMG_HEIGHT = 14000

death_pos = [DEATH_IMG_WIDTH/2,DEATH_IMG_HEIGHT/2]

while death_image.get_width() == 0:
    pass

transfer_image = simplegui.load_image("https://i.imgur.com/ukdZj81.png")

TRANSFER_COLS = 5
TRANSFER_ROWS = 2

TRANSFER_IMG_WIDTH = 1920
TRANSFER_IMG_HEIGHT = 980

while transfer_image.get_width() == 0:
    pass

go_hand_image = simplegui.load_image("https://i.imgur.com/1Tadgne.png")

GO_HAND_SIZE = (256, 256)
GO_HAND_COLS = 3
GO_HAND_ROWS = 2

GO_HAND_IMG_WIDTH = 256
GO_HAND_IMG_HEIGHT = 256

dialogue_image = simplegui.load_image("https://i.imgur.com/QnV1AwY.png")

DIALOGUE_SIZE = (1920, 980)
DIALOGUE_COLS = 10
DIALOGUE_ROWS = 2

DIALOGUE_IMG_WIDTH = 1920
DIALOGUE_IMG_HEIGHT = 980

# player attributes

PLAYER_SPEED = 5

BOT_SPEED = 3

GUARD_SPEED = 8

# Canvas size
WIDTH = 1920
HEIGHT = 980


PLAYER_DIRECTION = 'right'
PLAYER_SIZE = (256,256)

#bullet attributes
BULLET_SPEED = 35

#background attributes
current_background = 0


BGRD_WIDTH = [bgrd_image[0].get_width(),
              bgrd_image[1].get_width(),
              bgrd_image[2].get_width(),
              bgrd_image[3].get_width(),
              bgrd_image[4].get_width()]


BGRD_HEIGHT = [bgrd_image[0].get_height(),
               bgrd_image[1].get_height(),
               bgrd_image[2].get_height(),
               bgrd_image[3].get_height(),
               bgrd_image[4].get_height()]

background_pos = [BGRD_WIDTH[current_background]/2,BGRD_HEIGHT[current_background]/2]

#make sure bgrd image is loaded, for current, the rest load as the level starts
for i in range(len(bgrd_image)):
    while bgrd_image[i].get_width() == 0:
        pass
    
#    
#sound
bgrd_sound = simplegui.load_sound("https://opengameart.org/sites/default/files/TremLoadingloopl.wav")
main_menu_music = simplegui.load_sound("https://drive.google.com/file/d/1FR3wyVb6aXAbnwL5bZIBSDy9Ujbo977Z/view?usp=sharing")
death_music = simplegui.load_sound("https://opengameart.org/sites/default/files/bleeding_out2_2.ogg")
ak_sound = simplegui.load_sound("https://retired.sounddogs.com/previews/44/mp3/494380_SOUNDDOGS__gu.mp3")
ak_guard_sound = simplegui.load_sound("https://retired.sounddogs.com/previews/44/mp3/494380_SOUNDDOGS__gu.mp3")
pistol_sound = simplegui.load_sound("https://retired.sounddogs.com/previews/2665/mp3/1132656_SOUNDDOGS__si.mp3")
ar_sound = simplegui.load_sound("https://retired.sounddogs.com/previews/2665/mp3/1132845_SOUNDDOGS__m4.mp3")
shotgun_sound = simplegui.load_sound("https://retired.sounddogs.com/previews/25/mp3/267025_SOUNDDOGS__gu.mp3")
empty_sound = simplegui.load_sound("https://retired.sounddogs.com/previews/25/mp3/309407_SOUNDDOGS__gu.mp3")
reload_sound = simplegui.load_sound("https://retired.sounddogs.com/previews/25/mp3/270729_SOUNDDOGS__gu.mp3")
click_sound = simplegui.load_sound("https://opengameart.org/sites/default/files/Menu%20Selection%20Click.wav")

#health values
assault_health = 10
defender_health = 8
scout_health = 14
player_health = 200
guard_health = 50

#inaccuracy values
player_inaccuracy = 8
scout_inaccuracy = 5
assault_inaccuracy = 10
guard_inaccuracy = 15

#damage values
player_attack = 6
assault_attack = 3
defender_attack = 1
scout_attack = 2
guard_attack = 4

#time multiplier is for roll speed
time_multiplier = 1

#self explanatory
magazine_size = 60
total_magazines = 20

#the distance which tells how close enemies want to be
engagement_distance = 600

#for making the background stay in place and correctly move when needed
borders = [BGRD_WIDTH[current_background]/2, (WIDTH-BGRD_WIDTH[current_background]/2)]
middle = WIDTH/2

#if in menu
menu = True

#if dead
death = False

#if in screen change
transfer = False

#run credit:
credit = True

#
dialogue = False

#lists of things that need to be checked
overlays = []
bullets = []
blood = []
walls = []
objects = []


#for spawning when player gets to certain place

#spawns indicate invisble tripwires which correspond to a wave of enemies in the enemy list

forward = WIDTH+128
behind = -128

spawns = [[300,500,800,1300,1500,1800,2500],
          [300,800,1500,1600,1700,1800,2000,2800],
          [300,800,1500,1600,1700,1800,2000,2800,3000,3500,4000,4500,4750,5500],
          [300,800,1500,1600,1700,1800,2000,2500,26502800,3000,3500,4000,4500,4750,5500],
          [300,800,1500]]

enemy = [{300:[['t',2]],500:[['s',forward,700]], 800:[['a',forward,700],['d',forward,800]], 1300:[['a',behind,700],['d',behind,800]], 1500:[['s',behind,700],['s',behind,800],['d',forward,700],['d',forward,800]], 1800:[['a',behind,700],['s',behind,800],['d',forward,700],['d',forward,600],['s',forward,650],['d',forward,800]], 2500:[['s',behind,750]]},
         {300:[['t',2]],800:[['s',forward,700], ['s',forward,750], ['s',forward,650]], 1500:[['a',forward,700],['d',forward,800]], 1600:[['a',forward,700]], 1700:[['a',forward,700],['a',forward,800]], 1800:[['a',behind,700],['a',behind,800]], 2000:[['s',forward,700],['s',forward,750],['s',forward,775],['s',forward,800],['d',behind,710],['d',behind,720],['a',behind,675]], 2800:[['a',behind,700],['d',behind,800]]},
         {300:[['t',3]],800:[['a',forward,700], ['s',forward,750], ['s',forward,650]], 1500:[['d',forward,700],['d',forward,800]], 1600:[['s',forward,700]], 1700:[['a',forward,700],['a',forward,800]], 1800:[['a',behind,700],['d',behind,800]], 2000:[['s',forward,700],['s',forward,750],['s',forward,775],['a',forward,800],['d',behind,710],['s',behind,720],['a',behind,675]], 2800:[['s',behind,700],['d',behind,800]], 3000:[['a',behind,700],['a',behind,800]], 3500:[['s',forward,750],['s',forward,700],['s',behind,700],['d',behind,800]],4000:[['a',behind,700],['s',behind,800],['d',forward,700],['d',forward,600],['s',forward,650],['d',forward,800]],4500:[['d',behind,700],['s',behind,800],['d',forward,700],['d',forward,800]],4750:[['s',behind,700],['a',behind,720],['a',behind,760],['s',behind,800],['d',forward,700],['d',forward,800]],5500:[['g',behind,750]]},
         {300:[['t',1]],800:[['a',forward,700], ['s',forward,750], ['d',forward,650], ['a',forward,720], ['s',forward,730], ['d',forward,610]], 1500:[['a',forward,700],['d',forward,800]], 1600:[['s',forward,700],['a',behind,720],['a',behind,800] ], 1700:[['c'],['a',forward,700],['a',forward,800]], 1800:[['a',behind,700],['d',behind,800],['d',behind,790],['d',behind,780],['d',behind,770]], 2000:[['a',forward,700],['s',forward,750],['s',forward,775],['a',forward,800],['d',behind,710]],2500:[['s',behind,720],['a',behind,675],['d',forward,800],['d',behind,710],['s',behind,705]],2650:[['a',behind,655]], 2800:[['s',behind,700],['d',behind,800]], 3000:[['a',behind,700],['a',behind,800]], 3500:[['c'],['s',forward,750],['s',forward,700],['s',behind,700],['s',behind,800]],4000:[['s',behind,700],['s',behind,800],['d',forward,700],['d',forward,600],['d',forward,650],['d',forward,800]],4500:[['d',behind,700],['s',behind,800],['d',forward,700],['d',forward,800]],4750:[['s',behind,700],['a',behind,720],['a',behind,760],['s',behind,800],['d',behind,690],['d',behind,800]],5500:[['d',behind,750]]},
         {300:[['t',2]],800:[['r',forward,700]],1500:[['g',forward,650],['g',forward,750],['g',behind,700]]}]

#start a new session, just the menu
def new_session():
    global transferoverlay
    
    transferoverlay = TransferOverlay((TRANSFER_IMG_WIDTH/2,TRANSFER_IMG_HEIGHT/2), transfer_image)
    overlays.append(transferoverlay)

#starts a new game, player, overlays sounds etc.
def new_game():
    global player, tens, ones, mags1, mags10, go_hand, current_background, transferoverlay, menu, borders, dialogueoverlay, bleedoverlay
    menu = False
    current_background = 0
    borders = [BGRD_WIDTH[current_background]/2, (WIDTH-BGRD_WIDTH[current_background]/2)]
    background_pos[0] = BGRD_WIDTH[current_background]/2

    player = Character(player_image, [300,700], [0,0], 'right')
    objects.append(player)
    tens = Number([30, 30], number_image)
    overlays.append(tens)
    ones = Number([30+NUMBER_IMG_WIDTH+10, 30], number_image)
    overlays.append(ones)
    mags10 = Number([30, 30+10+NUMBER_IMG_HEIGHT], number_image)
    mags1 = Number([30+NUMBER_IMG_WIDTH+10, 30+10+NUMBER_IMG_HEIGHT], number_image)
    overlays.append(mags1)
    overlays.append(mags10)
    go_hand = GoHand([WIDTH-150, 150], go_hand_image)
    overlays.append(go_hand)
    bleedoverlay = BleedOverlay((BLEEDOVERLAY_IMG_WIDTH/2,BLEEDOVERLAY_IMG_HEIGHT/2), bleedoverlay_image)
    overlays.append(bleedoverlay)
    dialogueoverlay = DialogueOverlay((DIALOGUE_IMG_WIDTH/2,DIALOGUE_IMG_HEIGHT/2), dialogue_image)
    overlays.append(dialogueoverlay)
    bgrd_sound.set_volume(0.1)
    death_music.set_volume(0.6)

# resets the objects and other variables and replaces spawnpoints of enemies
def reset():
    global overlays, bullets, blood, walls, objects, menu, death, transfer, transferoverlay, spawns, enemy, PLAYER_SPEED
    spawns = [[300,500,800,1300,1500,1800,2500],
              [300,800,1500,1600,1700,1800,2000,2800],
              [300,800,1500,1600,1700,1800,2000,2800,3000,3500,4000,4500,4750,5500],
              [300,800,1500,1600,1700,1800,2000,2500,26502800,3000,3500,4000,4500,4750,5500],
              [300,800,1500]]

    enemy = [{300:[['t',2]],500:[['s',forward,700]], 800:[['a',forward,700],['d',forward,800]], 1300:[['a',behind,700],['d',behind,800]], 1500:[['s',behind,700],['s',behind,800],['d',forward,700],['d',forward,800]], 1800:[['a',behind,700],['s',behind,800],['d',forward,700],['d',forward,600],['s',forward,650],['d',forward,800]], 2500:[['s',behind,750]]},
             {300:[['t',2]],800:[['s',forward,700], ['s',forward,750], ['s',forward,650]], 1500:[['a',forward,700],['d',forward,800]], 1600:[['a',forward,700]], 1700:[['a',forward,700],['a',forward,800]], 1800:[['a',behind,700],['a',behind,800]], 2000:[['s',forward,700],['s',forward,750],['s',forward,775],['s',forward,800],['d',behind,710],['d',behind,720],['a',behind,675]], 2800:[['a',behind,700],['d',behind,800]]},
             {300:[['t',3]],800:[['a',forward,700], ['s',forward,750], ['s',forward,650]], 1500:[['d',forward,700],['d',forward,800]], 1600:[['s',forward,700]], 1700:[['a',forward,700],['a',forward,800]], 1800:[['a',behind,700],['d',behind,800]], 2000:[['s',forward,700],['s',forward,750],['s',forward,775],['a',forward,800],['d',behind,710],['s',behind,720],['a',behind,675]], 2800:[['s',behind,700],['d',behind,800]], 3000:[['a',behind,700],['a',behind,800]], 3500:[['s',forward,750],['s',forward,700],['s',behind,700],['d',behind,800]],4000:[['a',behind,700],['s',behind,800],['d',forward,700],['d',forward,600],['s',forward,650],['d',forward,800]],4500:[['d',behind,700],['s',behind,800],['d',forward,700],['d',forward,800]],4750:[['s',behind,700],['a',behind,720],['a',behind,760],['s',behind,800],['d',forward,700],['d',forward,800]],5500:[['g',behind,750]]},
             {300:[['t',1]],800:[['a',forward,700], ['s',forward,750], ['d',forward,650], ['a',forward,720], ['s',forward,730], ['d',forward,610]], 1500:[['a',forward,700],['d',forward,800]], 1600:[['s',forward,700],['a',behind,720],['a',behind,800] ], 1700:[['c'],['a',forward,700],['a',forward,800]], 1800:[['a',behind,700],['d',behind,800],['d',behind,790],['d',behind,780],['d',behind,770]], 2000:[['a',forward,700],['s',forward,750],['s',forward,775],['a',forward,800],['d',behind,710]],2500:[['s',behind,720],['a',behind,675],['d',forward,800],['d',behind,710],['s',behind,705]],2650:[['a',behind,655]], 2800:[['s',behind,700],['d',behind,800]], 3000:[['a',behind,700],['a',behind,800]], 3500:[['c'],['s',forward,750],['s',forward,700],['s',behind,700],['s',behind,800]],4000:[['s',behind,700],['s',behind,800],['d',forward,700],['d',forward,600],['d',forward,650],['d',forward,800]],4500:[['d',behind,700],['s',behind,800],['d',forward,700],['d',forward,800]],4750:[['s',behind,700],['a',behind,720],['a',behind,760],['s',behind,800],['d',behind,690],['d',behind,800]],5500:[['d',behind,750]]},
             {300:[['t',2]],800:[['r',forward,700]],1500:[['g',forward,650],['g',forward,750],['g',behind,700]]}]
    death_music.rewind()
    bgrd_sound.set_volume(1)
    transfer = False
    PLAYER_SPEED = 4
    death = False
    menu = True
    overlays = []
    bullets = []
    blood = []
    walls = []
    objects = []
    transferoverlay = TransferOverlay((TRANSFER_IMG_WIDTH/2,TRANSFER_IMG_HEIGHT/2), transfer_image)
    overlays.append(transferoverlay)
    
    
 
#inbounds detection    
def inbounds(pos, width, height):
    in_x = pos[0] > 0 and pos[0] < WIDTH
    in_y = pos[1] > 117*4 + height/2 and pos[1] < HEIGHT - height/2
    return in_x, in_y

#inmap detection    
def inmap(pos, width, height):
    in_x = pos[0] > (background_pos[0]-BGRD_WIDTH[current_background]/2) and pos[0] < (background_pos[0]+BGRD_WIDTH[current_background]/2)
    in_y = pos[1] > 117*4 + height/2 and pos[1] < BGRD_HEIGHT[current_background] - height/2 #117*4 is to keep the player from going to high because of how the game is designed
    return in_x, in_y

#helper function for who to draw first
def object_y(object):
    return object.pos[1]

#finds which ditection to face given self and enemy coords
def enemy_direction(coords_self, coords_enemy):
    if coords_self[0] > coords_enemy[0]:
        return 'left'
    else:
        return 'right'
#finds if an enemy is above or below you on the axis  
def enemy_elevation(coords_self, coords_enemy):
    if coords_self[1] > coords_enemy[1]:
        return 'down'
    elif coords_self[1] < coords_enemy[1]:
        return 'up'

    
#used to iterate through spawns and enemy waves to handle enemy spawning
def check_spawn_enemies(pos):
    global spawns, objects, dialogueoverlay, dialogue
    for s in range(len(spawns[current_background])):
        if abs(pos-spawns[current_background][s-1]) <= PLAYER_SPEED:
            for item in enemy[current_background][spawns[current_background][s-1]]:
                if item[0] == 'a':
                    bot = Assault(assault_image, [item[1],item[2]], [0,0], 'right')
                    objects.append(bot)
                elif item[0] == 'd':
                    bot = Defender(defender_image, [item[1],item[2]], [0,0], 'right')
                    objects.append(bot)
                elif item[0] == 's':
                    bot = Scout(scout_image, [item[1],item[2]], [0,0], 'right')
                    objects.append(bot)
                elif item[0] == 'g':
                    bot = Guard(guard_image, [item[1],item[2]], [0,0], 'right')
                    objects.append(bot)
                elif item[0] == 'r':
                    bot = Reshala(reshala_image, [item[1],item[2]], [0,0], 'right')
                    objects.append(bot)
                elif item[0] == 't':#used to active the text dialogues
                    dialogueoverlay.amount = item[1]
                    dialogue = True
            spawns[current_background].remove(spawns[current_background][s-1])
#moves the background in the menu for aesthic reasons
def bgrd_move():
    global current_background
    background_pos[0]-=2
    if background_pos[0] < BGRD_WIDTH[current_background]/4:
        if current_background+1 < len(BGRD_WIDTH):
            current_background+=1
            background_pos[0] = BGRD_WIDTH[current_background]/2
        else:
            current_background = 0
            background_pos[0] = BGRD_WIDTH[current_background]/2
            
#switches map if avaliable  
def next_map():
    global current_background, borders, background_pos, objects, transferoverlay, player, bleedoverlay, PLAYER_SPEED
    if current_background+1 == len(bgrd_image):
        pass
        #game end
    #makes sure there are no bots than begins the process, darken screen brighten 
    else:
        go = True
        for o in objects:
            if o.type == 'bot':
                if o.alive:
                    go = False
        if go:
            transferoverlay.state = True
            if transferoverlay.switch:
                player.health = player_health
                if bleedoverlay.time != -1:
                    PLAYER_SPEED = 3
                bleedoverlay.time = -1

                transferoverlay.switch = False
                go = True
                current_background+=1
                background_pos = [BGRD_WIDTH[current_background]/2,BGRD_HEIGHT[current_background]/2]
                borders = [BGRD_WIDTH[current_background]/2, (WIDTH-BGRD_WIDTH[current_background]/2)]
                player.pos[0] = 0
                while len(objects) > 1:
                    for o in objects:
                        if o.type != 'player':
                            objects.remove(o)

#used to display numbers for ammo and magazines   
class Number:
    def __init__(self, position, image):
        self.pos = position
        self.image = image
        self.state = -1
        self.time = 0

    def draw(self, canvas):
        if self.state != -1 or self.time <= 200:
            col = int(self.state)%NUMBER_COLS
            row = int(self.state)//NUMBER_COLS
            center_x = NUMBER_IMG_WIDTH/2+ col*NUMBER_IMG_WIDTH
            center_y = NUMBER_IMG_HEIGHT/2 +row*NUMBER_IMG_HEIGHT
            canvas.draw_image(self.image, 
                              (center_x, center_y), 
                              (NUMBER_IMG_WIDTH, NUMBER_IMG_HEIGHT), 
                              self.pos, 
                              (NUMBER_SIZE))
        
    def update(self): #just draw the current frame on animation, at a slow pace
        self.time += 1
        if self.time == 200:
            self.state = -1

#used to tell player to push up or stop
class GoHand:
    def __init__(self, position, image):
        self.pos = position
        self.image = image
        self.state = -1
        self.time = 0
        self.check_time = 0

    def draw(self, canvas):
        if self.state != -1:
            col = int(self.time)%GO_HAND_COLS
            row = int(self.time)//GO_HAND_COLS
            center_x = GO_HAND_IMG_WIDTH/2+ col*GO_HAND_IMG_WIDTH
            center_y = GO_HAND_IMG_HEIGHT/2 +row*GO_HAND_IMG_HEIGHT
            canvas.draw_image(self.image, 
                              (center_x, center_y), 
                              (GO_HAND_IMG_WIDTH, GO_HAND_IMG_HEIGHT), 
                              self.pos, 
                              (GO_HAND_SIZE))
        
    def update(self): #just draw the current frame on animation, at a slow pace
        self.time += 0.1
        if int(self.time) == GO_HAND_COLS * GO_HAND_ROWS:
            self.time = 0
        self.check_time+=0.1
        if int(self.check_time) == 10:
            self.check_time = 0
            go = True
            for o in objects:
                if o.type == 'bot':
                    if o.alive:
                        go = False
            if go:
                go = True
                self.state = 1
            else:
                go = False
                self.state = -1
#bullet used for all enemies/ player       
class Bullet:
    def __init__(self, position, velocity, image, owner, attack):
        self.pos = position
        self.vel = velocity
        self.img = image
        self.own = owner
        self.attack = attack
        
    def draw(self, canvas):
        canvas.draw_image(self.img, 
                          (BULLET_IMG_WIDTH/2,BULLET_IMG_HEIGHT/2), 
                          (BULLET_IMG_WIDTH,BULLET_IMG_HEIGHT),
                          self.pos, 
                          BULLET_SIZE)

    def update(self):
        for o in objects:
            if abs((o.pos[0])-(self.pos[0])) <= 48 and abs((o.pos[1])-(self.pos[1])-BULLET_IMG_HEIGHT) <= 32: #check to see if hit anything
                if o.type != self.own and not o.dodge: #if object is dodging, bullet keeps on going, else delete bullet do damage
                    o.damage(self.attack)
                    if self in bullets:
                        bullets.remove(self)
        for i in range(2):
            self.pos[i] += self.vel[i]
            
            
# the little credits/ special thanks thing at the beggining for Jaden, who helped out with some art
class CreditOverlay:
    def __init__(self, position, image):
        self.pos = position
        self.image = image
        self.time = 0
        self.state = True

    def draw(self, canvas):
        if self.state:
            col = int(self.time)%CREDIT_COLS
            row = int(self.time)//CREDIT_COLS
            center_x = CREDIT_IMG_WIDTH/2+ col*CREDIT_IMG_WIDTH
            center_y = CREDIT_IMG_HEIGHT/2 +row*CREDIT_IMG_HEIGHT
            canvas.draw_image(self.image, 
                              (center_x, center_y), 
                              (CREDIT_IMG_WIDTH, CREDIT_IMG_HEIGHT), 
                              self.pos, 
                              (WIDTH,HEIGHT))
        
    def update(self): #just draw the current frame on animation, at a slow pace
        global overlays
        if self.state:
            self.time +=0.1
            if int(self.time) == int(CREDIT_ROWS*CREDIT_COLS):
                self.state = False
                overlays.remove(self)
            
# the red pulsating screen when you are injured badly, reduces speed      
class BleedOverlay:
    def __init__(self, position, image):
        self.pos = position
        self.image = image
        self.time = -1

    def draw(self, canvas):
        if self.time != -1:
            col = int(self.time)%BLEEDOVERLAY_COLS
            row = int(self.time)//BLEEDOVERLAY_COLS
            center_x = BLEEDOVERLAY_IMG_WIDTH/2+ col*BLEEDOVERLAY_IMG_WIDTH
            center_y = BLEEDOVERLAY_IMG_HEIGHT/2 +row*BLEEDOVERLAY_IMG_HEIGHT
            canvas.draw_image(self.image, 
                              (center_x, center_y), 
                              (BLEEDOVERLAY_IMG_WIDTH, BLEEDOVERLAY_IMG_HEIGHT), 
                              self.pos, 
                              (WIDTH,HEIGHT))
        
    def update(self): #just draw the current frame on animation, at a slow pace
        global PLAYER_SPEED
        if player.health <= 3:
            PLAYER_SPEED = 2 #lower player speed
            self.time +=0.05
            self.time %= BLEEDOVERLAY_ROWS*BLEEDOVERLAY_COLS
            self.state = False

#the reflection screen about your death with the speech thing
class DeathOverlay:
    def __init__(self, position, image):
        self.pos = position
        self.image = image
        self.time = 0
        self.state = False

    def draw(self, canvas):
        if self.state and self.time >= 300:
            canvas.draw_image(death_image,(DEATH_IMG_WIDTH/2,DEATH_IMG_HEIGHT/2),(DEATH_IMG_WIDTH, DEATH_IMG_HEIGHT), self.pos,(DEATH_IMG_WIDTH,DEATH_IMG_HEIGHT))
        
    def update(self): #just draw the current frame on animation, at a slow pace
        global menu, transferoverlay, deathoverlay, overlay, bullets, blood, walls, objects
        self.time+=1
        if self.state and self.pos[1] != (HEIGHT-DEATH_IMG_HEIGHT/2) and self.time >= 300:
            bullets = []
            blood = []
            walls = []
            objects = []
            self.pos[1]-=1

#the overlay that transitions some scenes by going dark and brightning up again
class TransferOverlay:
    def __init__(self, position, image):
        self.pos = position
        self.image = image
        self.time = -1
        self.state = False
        self.switch = False
        self.done = False

    def draw(self, canvas):
        if self.time != -1:
            col = int(self.time)%TRANSFER_COLS
            row = int(self.time)//TRANSFER_COLS
            center_x = TRANSFER_IMG_WIDTH/2+ col*TRANSFER_IMG_WIDTH
            center_y = TRANSFER_IMG_HEIGHT/2 +row*TRANSFER_IMG_HEIGHT
            canvas.draw_image(self.image, 
                              (center_x, center_y), 
                              (TRANSFER_IMG_WIDTH, TRANSFER_IMG_HEIGHT), 
                              self.pos, 
                              (WIDTH,HEIGHT))
        
    def update(self): #just draw the current frame on animation, at a slow pace
        if self.state:
            self.time +=0.1
            if int(self.time) == TRANSFER_ROWS*TRANSFER_COLS:
                self.done = False
                self.time = -1
                self.state = False
                self.switch = False
            if int(self.time) == int((TRANSFER_ROWS*TRANSFER_COLS)/2) and (not self.done):
                self.switch = True
                self.done = True

        
#dialogue class things, just a spritesheet of all the dialogues
class DialogueOverlay:
    def __init__(self, position, image):
        self.pos = position
        self.image = image
        self.state = 0
        self.amount = 0

    def draw(self, canvas):
        if self.amount > 0:
            col = int(self.state)%DIALOGUE_COLS
            row = int(self.state)//DIALOGUE_COLS
            center_x = DIALOGUE_IMG_WIDTH/2+ col*DIALOGUE_IMG_WIDTH
            center_y = DIALOGUE_IMG_HEIGHT/2 +row*DIALOGUE_IMG_HEIGHT
            canvas.draw_image(self.image, 
                              (center_x, center_y), 
                              (DIALOGUE_IMG_WIDTH, DIALOGUE_IMG_HEIGHT), 
                              self.pos, 
                              (WIDTH,HEIGHT))
   
    def update(self): #choose which dialogue
        pass
        #so i dont have to give a custom condition that the overlay update has to skip over
        
#the blood splatter that happens when you take damage or enemies take damage to help visualize a hit       
class Blood:
    def __init__(self, position, image, state):
        self.pos = position
        self.image = image
        self.time = 0
        self.state = state

    def draw(self, canvas):
        col = int(self.time)%BLOOD_COLS[self.state]
        row = int(self.time)//BLOOD_COLS[self.state]
        center_x = BLOOD_IMG_WIDTH[self.state]/2+ col*BLOOD_IMG_WIDTH[self.state]
        center_y = BLOOD_IMG_HEIGHT[self.state]/2 +row*BLOOD_IMG_HEIGHT[self.state]
        canvas.draw_image(self.image, 
                          (center_x, center_y), 
                          (BLOOD_IMG_WIDTH[self.state], BLOOD_IMG_HEIGHT[self.state]), 
                          self.pos, 
                          BLOOD_SIZE)
    def update(self): #just a quick animation for blood
        self.time +=0.1
        if int(self.time) == BLOOD_ROWS[self.state]*BLOOD_COLS[self.state]:
            blood.remove(self)

#there was plans to add run down cars and junk to block the way, but do to time constraint and it interfering with the gameplay was decided to not be implemented
class Wall:
    def __init__(self, left,right,top,bottom):
        self.left = left
        self.right = right
        self.top = top
        self.bot = bottom
        self.corners = [[self.left,self.top],
                        [self.right,self.top],
                        [self.right,self.bot],
                        [self.left,self.bot]]            
    # For testing only        
    def draw(self, canvas):
        canvas.draw_polygon(self.corners,2,"white","white")

    def collide(self, pos, width, height):
        in_x = pos[0] > self.left - width/2 and pos[0] < self.right + width/2
        in_y = pos[1] > self.top - height/2 and pos[1] < self.bot + height/2
        return in_x, in_y
    

class Character:
    def __init__(self, image, position, velocity, direction):
        self.type = 'player'
        self.p_image = image
        self.state = 'walk_right' #which animation to use
        self.image = image[self.state]
        self.pos = position
        self.vel = velocity
        self.time = 0
        self.stuck = False # if the character can preform any other animations
        self.direction = direction # last known direction that the character faced
        self.shooting = False
        self.stop = False # for control of fire rate
        self.dodge = False
        self.reloading = False
        self.checking = False
        
        self.width = PLAYER_IMG_WIDTH[self.state]
        self.height = PLAYER_IMG_HEIGHT[self.state]
        
        self.ammo = magazine_size
        self.magazines = total_magazines
        
        self.health = player_health
        self.attack = player_attack
        self.alive = True
        
    def shoot(self): #shooting, y vel is random for inaccuracy
        self.ammo-=1
        if self.direction == 'right':
            #shooting is just spawning a bullet going in the correct direction out of the gun with an inaccuracy to add gameplay elements and make shooting less bland
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED,(random.randint(-player_inaccuracy,player_inaccuracy)/10)], bullet_image, self.type, self.attack)
        else:
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED,(random.randint(-player_inaccuracy,player_inaccuracy)/10)], bullet_image, self.type, self.attack)
        bullets.append(bullet)
        if ones.time < 200: #live updates on ammo
            
            #updates the ammo counter so one can see the live update when shooting ammo
            tens.time = 0
            ones.time = 0
            mags1.time = 0
            mags10.time = 0
            ones.state = (self.ammo%10)
            tens.state = (self.ammo - (self.ammo%10))//10
            mags1.state = (self.magazines%10)
            mags10.state = (self.magazines - (self.magazines%10))//10
        
    def damage(self, damage): #create a blood effect and take damage
        if self.health > 0 and not self.dodge:
            self.health-=damage
            img = blood_image['blood_right'] if self.direction == 'right' else blood_image['blood_left']
            blood_effect = Blood(self.pos, img, ('blood_right' if self.direction == 'right' else 'blood_left'))
            blood.append(blood_effect)
        if self.health <= 0 and self.alive:
            self.dodge = True
            self.time = 0
            self.alive = False
            self.stuck = True
            self.vel =[0,0]
            self.state = 'death_right' if self.direction == 'right' else 'death_left'
        
    def roll(self): #dodge bullets and prepare for animation of roll
        global time_multiplier
        time_multiplier = 2
        self.stuck = True
        self.time = 0
        self.dodge = True
        self.state = 'roll_right' if self.direction == 'right' else 'roll_left'
        self.vel[0] = PLAYER_SPEED if self.direction == 'right' else -PLAYER_SPEED
        
    def reload(self): #remove a magazine refill ammo
        self.ammo = magazine_size
        self.magazines-=1
        self.reloading = True
        self.stuck = True
        self.time = 0
        self.vel = [0,0]
        self.state = 'reload_right' if self.direction == 'right' else 'reload_left'
    
    def check(self): #check ammo 
        self.reloading = True
        self.stuck = True
        self.time = 0
        self.vel = [0,0]
        self.state = 'check_right' if self.direction == 'right' else 'check_left'
        
        tens.time = 0
        ones.time = 0
        mags1.time = 0
        mags10.time = 0
        ones.state = (self.ammo%10)
        tens.state = (self.ammo - (self.ammo%10))//10
        mags1.state = (self.magazines%10)
        mags10.state = (self.magazines - (self.magazines%10))//10
        
    def draw(self, canvas): #draw function used for almost all the objects in the game
        col = int(self.time)%PLAYER_COLS[self.state]
        row = int(self.time)//PLAYER_COLS[self.state]
        center_x = PLAYER_IMG_WIDTH[self.state]/2+ col*PLAYER_IMG_WIDTH[self.state]
        center_y = PLAYER_IMG_HEIGHT[self.state]/2 +row*PLAYER_IMG_HEIGHT[self.state]
        canvas.draw_image(self.image, 
                          (center_x, center_y), 
                          (PLAYER_IMG_WIDTH[self.state], PLAYER_IMG_HEIGHT[self.state]), 
                          self.pos, 
                          PLAYER_SIZE)
        
    def update(self): #all animations done here
        global image, time_multiplier, middle
        self.image = player_image[self.state]
        
        next_pos = [self.pos[0] + self.vel[0], self.pos[1] + self.vel[1]]        
        wall_collision_x = False
        wall_collision_y = False
        
        for wall in walls:
            if wall.collide(next_pos, PLAYER_IMG_WIDTH[self.state], PLAYER_IMG_HEIGHT[self.state])[0]:
                wall_collision_x = True
            if wall.collide(next_pos, PLAYER_IMG_WIDTH[self.state], PLAYER_IMG_HEIGHT[self.state])[1]:
                wall_collision_y = True
                
        if not wall_collision_x and inbounds(next_pos, PLAYER_IMG_WIDTH[self.state], PLAYER_IMG_HEIGHT[self.state])[0]:
            #update the x position on the x velocity
            
            #check if spawn in enemies
            check_spawn_enemies(abs(background_pos[0]-BGRD_WIDTH[current_background]/2)+self.pos[0])          
            
            #player movement: if at border then dont move background, if not and at the middle of the screen move the border, otherwise the player moves freeely
            if background_pos[0]-self.vel[0] >= borders[0] or background_pos[0]-self.vel[0] <= borders[1]: #if at border move player
                self.pos[0] += self.vel[0]
                
            elif abs(middle-next_pos[0]) <= PLAYER_SPEED: #if at mid move background
                self.pos[0] = middle
                background_pos[0] -= self.vel[0]
                for o in objects:
                    if o.type != 'player':
                        o.pos[0] -= self.vel[0]
            else:
                self.pos[0] += self.vel[0]
        elif next_pos[0] >= WIDTH:
            #if next position goes out of the map on the right side then go to the next map
            next_map()
                
        if not wall_collision_y and inbounds(next_pos, PLAYER_IMG_WIDTH[self.state], PLAYER_IMG_HEIGHT[self.state])[1]:    
            #update the y position
            self.pos[1] += self.vel[1]       
        if self.vel != [0, 0] and self.alive:
            self.time+=0.1*time_multiplier
            if self.dodge and int(self.time) == PLAYER_ROWS[self.state]*PLAYER_COLS[self.state]: #rolling animation and dodges bullets
                self.stuck = False
                self.dodge = False
                time_multiplier = 1
                self.vel = [0,0]
                self.state = 'walk_right' if player.direction == 'right' else 'walk_left'
            self.time %= PLAYER_ROWS[self.state]*PLAYER_COLS[self.state]
            
        if self.reloading and self.alive: #reloading animation and stop moving
            self.time+=0.1
            reload_sound.play()
            if int(self.time) == PLAYER_ROWS[self.state]*PLAYER_COLS[self.state]:
                reload_sound.rewind()
                self.time = 0
                self.stuck = False
                self.reloading = False
                self.vel = [0,0]
                self.state = 'walk_right' if player.direction == 'right' else 'walk_left'
            self.time %= PLAYER_ROWS[self.state]*PLAYER_COLS[self.state]
            
        if self.shooting and self.alive: # if player is shooting left or right  
            self.stuck = True
            if round(self.time, 1) == 0.2: #shoots on the frame of muzzle flash
                ak_sound.rewind()
                ak_sound.play()
                player.shoot()
            self.time +=0.1
            if int(self.time) == PLAYER_ROWS[self.state]*PLAYER_COLS[self.state]: 
                self.time = 0
                if self.stop or self.ammo <= 0:
                    self.state = 'walk_right' if player.direction == 'right' else 'walk_left'
                    self.shooting = False
                    self.stuck = False
        
        if not self.alive: #goes to death screen, gameover
            bgrd_sound.rewind()
            death_music.play()
            self.stuck = True
            if int(self.time) == PLAYER_ROWS[self.state]*PLAYER_COLS[self.state]-1:
                pass
                #gameover
            else:
                self.time+=0.1
                
    
#bots
class Reshala: #the boos, does nothing except look at you
    def __init__(self, image, position, velocity, direction):
        self.type = 'boss with no skill/bravery and only money'
        self.p_image = image
        self.state = 'walk_left' #which animation to use
        self.image = image[self.state]
        self.pos = position
        self.vel = velocity
        self.time = 0
        self.action_time = 0
        self.stuck = False # if the character can preform any other animations
        self.direction = direction # last known direction that the character faced
        self.dodge = True
        
        self.width = RESHALA_IMG_WIDTH[self.state]
        self.height = RESHALA_IMG_HEIGHT[self.state]
        
        self.stop = False
        
        
        
    def draw(self, canvas):
        col = int(0)%RESHALA_COLS[self.state]
        row = int(0)//RESHALA_COLS[self.state]
        center_x = RESHALA_IMG_WIDTH[self.state]/2+ col*RESHALA_IMG_WIDTH[self.state]
        center_y = RESHALA_IMG_HEIGHT[self.state]/2 +row*RESHALA_IMG_HEIGHT[self.state]
        canvas.draw_image(self.image, 
                          (center_x, center_y),
                          (RESHALA_IMG_WIDTH[self.state], RESHALA_IMG_HEIGHT[self.state]), 
                          self.pos, 
                          PLAYER_SIZE)
    def update(self):
        global image, dialogue, dialogueoverlay
        self.time+=0.1
        self.image = self.p_image[self.state]
        self.direction = enemy_direction(self.pos, player.pos)
        self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
        
        if int(self.time) == int(10):
            
            self.time = 0
            go = False
            if len(objects) > 2:
                go = True
                for o in objects:
                    if o.type == 'bot':
                        if o.alive:
                            go = False
            if go and not self.stop:
                dialogue = True
                dialogueoverlay.amount = 10
                self.stop = True
        
class Guard: #fast aggressive bot
    def __init__(self, image, position, velocity, direction):
        self.type = 'bot'
        self.p_image = image
        self.state = 'walk_left' #which animation to use
        self.image = image[self.state]
        self.pos = position
        self.vel = velocity
        self.time = 0
        self.action_time = 0
        self.stuck = False # if the character can preform any other animations
        self.direction = direction # last known direction that the character faced
        self.dodge = False
        
        self.width = GUARD_IMG_WIDTH[self.state]
        self.height = GUARD_IMG_HEIGHT[self.state]
        
        self.health = guard_health
        self.attack = guard_attack
        self.alive = True
        
    def damage(self, damage):
        if self.health >= 1:
            self.health-=damage
            img = blood_image['blood_right'] if self.direction == 'right' else blood_image['blood_left']
            blood_effect = Blood(self.pos, img, ('blood_right' if self.direction == 'right' else 'blood_left'))
            blood.append(blood_effect)
        if self.alive and self.health <= 0:
            self.alive = False
            self.stuck = True
            self.time = 0
            self.vel =[0,0]
            self.state = 'death_right' if self.direction == 'right' else 'death_left'
            self.dodge = True
    
    def ready_shoot(self): #set up variables to prepare shooting
        self.stuck = True
        self.shooting = True
        self.time = 0 # reset time
        self.vel = [0,0] # stop moving
        self.state = 'shoot_right' if self.direction == 'right' else 'shoot_left' # choose which animation to use based on last direction 
        
    def shoot(self): # spawn bullets
        if self.direction == 'right':
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED,(random.randint(-guard_inaccuracy,guard_inaccuracy)/10)], bullet_image, self.type, self.attack)
        else:
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED,(random.randint(-guard_inaccuracy,guard_inaccuracy)/10)], bullet_image, self.type, self.attack)
        bullets.append(bullet)
        
    def walk(self, direction): # moving the bot left and right
        distance = abs(player.pos[0]-self.pos[0])
        if direction == 'left' and distance >= engagement_distance:
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = -GUARD_SPEED
            return
        elif direction == 'left':
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = GUARD_SPEED
        if direction == 'right' and distance >= engagement_distance:
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = GUARD_SPEED
        elif direction == 'right':
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = -GUARD_SPEED
            
    def strafe(self, elevation): #moving up and down
        move = random.randint(1,10)
        if elevation == 'up':
            if move == 10:
                self.vel[1] = -GUARD_SPEED
            else:    
                self.vel[1] = GUARD_SPEED
            
        elif elevation == 'down':
            if move == 10:
                self.vel[1] = GUARD_SPEED
            else:    
                self.vel[1] = -GUARD_SPEED

        
    def draw(self, canvas): #animate the guard
        col = int(self.time)%GUARD_COLS[self.state]
        row = int(self.time)//GUARD_COLS[self.state]
        center_x = GUARD_IMG_WIDTH[self.state]/2+ col*GUARD_IMG_WIDTH[self.state]
        center_y = GUARD_IMG_HEIGHT[self.state]/2 +row*GUARD_IMG_HEIGHT[self.state]
        canvas.draw_image(self.image, 
                          (center_x, center_y),
                          (GUARD_IMG_WIDTH[self.state], GUARD_IMG_HEIGHT[self.state]), 
                          self.pos, 
                          PLAYER_SIZE)
    def update(self):
        global image
        self.image = self.p_image[self.state]
        
        next_pos = [self.pos[0] + self.vel[0], self.pos[1] + self.vel[1]]        
        wall_collision_x = False
        wall_collision_y = False
        
        if self.alive and inmap(self.pos, GUARD_IMG_WIDTH[self.state], GUARD_IMG_HEIGHT[self.state])[0]: #can move as long as in map, different from in screen (inbounds)
        
            for wall in walls:
                if wall.collide(next_pos, GUARD_IMG_WIDTH[self.state], GUARD_IMG_HEIGHT[self.state])[0]:
                    wall_collision_x = True
                if wall.collide(next_pos, GUARD_IMG_WIDTH[self.state], GUARD_IMG_HEIGHT[self.state])[1]:
                    wall_collision_y = True

            if not wall_collision_x and inmap(next_pos, GUARD_IMG_WIDTH[self.state], GUARD_IMG_HEIGHT[self.state])[0]:
                #update the x position on the x velocity
                self.pos[0] += self.vel[0]
            if not wall_collision_y and inmap(next_pos, GUARD_IMG_WIDTH[self.state], GUARD_IMG_HEIGHT[self.state])[1]:    
                #update the y position
                self.pos[1] += self.vel[1]       

            if self.vel != [0, 0] and self.alive: #moveing
                self.time+=0.1 
                if int(self.time) == GUARD_ROWS[self.state]*GUARD_COLS[self.state] or (abs(self.pos[1]-player.pos[1]) <= 6 and self.vel[0] == 0):
                    self.vel = [0,0]
                    self.time = 0

            elif not self.stuck and self.alive:
                self.action_time+=0.1 #delay to choose a move
                self.direction = enemy_direction(self.pos, player.pos)
                self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                if int(self.action_time) >= 1: #make a move
                    self.action_time = 0
                    choice = random.randint(1,6) # choose what to action to do
                    if choice == 1:
                        self.strafe(enemy_elevation(self.pos, player.pos))      
                    elif choice == 2:
                        self.walk(enemy_direction(self.pos, player.pos))
                    else:
                        if inbounds(self.pos, 0, GUARD_IMG_HEIGHT[self.state])[0]:
                            self.ready_shoot()       
                        


            if self.state == 'shoot_right' or self.state == 'shoot_left': # if player is shooting left or right
                self.time +=0.1
                if round(self.time, 1) == 1.0: #shoot on the correct frame
                    ak_guard_sound.rewind()
                    ak_guard_sound.play()
                    self.shoot()
                if int(self.time) == GUARD_ROWS[self.state]*GUARD_COLS[self.state]:
                    self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                    self.time = 0
                    self.stuck = False
         
        if not self.alive: #death
            self.stuck = True
            self.shooting = False
            if int(self.time) == GUARD_ROWS[self.state]*GUARD_COLS[self.state]-1:
                pass
                #is dead, keep body on screen
            else:
                self.time+=0.1
                
#########################################                
#ALL BOTS ARE STRUCTURED THE SAME WAY
#########################################

class Assault:
    def __init__(self, image, position, velocity, direction):
        self.type = 'bot'
        self.p_image = image
        self.state = 'walk_left' #which animation to use
        self.image = image[self.state]
        self.pos = position
        self.vel = velocity
        self.time = 0
        self.action_time = 0
        self.stuck = False # if the character can preform any other animations
        self.direction = direction # last known direction that the character faced
        self.dodge = False
        
        self.width = ASSAULT_IMG_WIDTH[self.state]
        self.height = ASSAULT_IMG_HEIGHT[self.state]
        
        self.health = assault_health
        self.attack = assault_attack
        self.alive = True
        
    def damage(self, damage):
        if self.health >= 1:
            self.health-=damage
            img = blood_image['blood_right'] if self.direction == 'right' else blood_image['blood_left']
            blood_effect = Blood(self.pos, img, ('blood_right' if self.direction == 'right' else 'blood_left'))
            blood.append(blood_effect)
        if self.alive and self.health <= 0:
            self.alive = False
            self.stuck = True
            self.time = 0
            self.vel =[0,0]
            self.state = 'death_right' if self.direction == 'right' else 'death_left'
            self.dodge = True
    
    def ready_shoot(self):
        self.stuck = True
        self.shooting = True
        self.time = 0 # reset time
        self.vel = [0,0] # stop moving
        self.state = 'shoot_right' if self.direction == 'right' else 'shoot_left' # choose which animation to use based on last direction 
        
    def shoot(self):
        if self.direction == 'right':
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED,(random.randint(-assault_inaccuracy,assault_inaccuracy)/10)], bullet_image, self.type, self.attack)
        else:
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED,(random.randint(-assault_inaccuracy,assault_inaccuracy)/10)], bullet_image, self.type, self.attack)
        bullets.append(bullet)
        
    def walk(self, direction):
        distance = abs(player.pos[0]-self.pos[0])
        if direction == 'left' and distance >= engagement_distance:
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = -BOT_SPEED
            return
        elif direction == 'left':
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = BOT_SPEED
        if direction == 'right' and distance >= engagement_distance:
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = BOT_SPEED
        elif direction == 'right':
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = -BOT_SPEED
            
    def strafe(self, elevation):
        move = random.randint(1,10)
        if elevation == 'up':
            if move == 10:
                self.vel[1] = -BOT_SPEED
            else:    
                self.vel[1] = BOT_SPEED
            
        elif elevation == 'down':
            if move == 10:
                self.vel[1] = BOT_SPEED
            else:    
                self.vel[1] = -BOT_SPEED

        
    def draw(self, canvas):
        col = int(self.time)%ASSAULT_COLS[self.state]
        row = int(self.time)//ASSAULT_COLS[self.state]
        center_x = ASSAULT_IMG_WIDTH[self.state]/2+ col*ASSAULT_IMG_WIDTH[self.state]
        center_y = ASSAULT_IMG_HEIGHT[self.state]/2 +row*ASSAULT_IMG_HEIGHT[self.state]
        canvas.draw_image(self.image, 
                          (center_x, center_y),
                          (ASSAULT_IMG_WIDTH[self.state], ASSAULT_IMG_HEIGHT[self.state]), 
                          self.pos, 
                          PLAYER_SIZE)
    def update(self):
        global image
        self.image = self.p_image[self.state]
        
        next_pos = [self.pos[0] + self.vel[0], self.pos[1] + self.vel[1]]        
        wall_collision_x = False
        wall_collision_y = False
        
        if self.alive and inmap(self.pos, ASSAULT_IMG_WIDTH[self.state], ASSAULT_IMG_HEIGHT[self.state])[0]:
        
            for wall in walls:
                if wall.collide(next_pos, ASSAULT_IMG_WIDTH[self.state], ASSAULT_IMG_HEIGHT[self.state])[0]:
                    wall_collision_x = True
                if wall.collide(next_pos, ASSAULT_IMG_WIDTH[self.state], ASSAULT_IMG_HEIGHT[self.state])[1]:
                    wall_collision_y = True

            if not wall_collision_x and inmap(next_pos, ASSAULT_IMG_WIDTH[self.state], ASSAULT_IMG_HEIGHT[self.state])[0]:
                #update the x position on the x velocity
                self.pos[0] += self.vel[0]
            if not wall_collision_y and inmap(next_pos, ASSAULT_IMG_WIDTH[self.state], ASSAULT_IMG_HEIGHT[self.state])[1]:    
                #update the y position
                self.pos[1] += self.vel[1]       

            if self.vel != [0, 0] and self.alive:
                self.time+=0.1 
                if int(self.time) == ASSAULT_ROWS[self.state]*ASSAULT_COLS[self.state] or (abs(self.pos[1]-player.pos[1]) <= 6 and self.vel[0] == 0):
                    self.vel = [0,0]
                    self.time = 0

            elif not self.stuck and self.alive:
                self.action_time+=0.1
                self.direction = enemy_direction(self.pos, player.pos)
                self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                if int(self.action_time) >= 1:
                    self.action_time = 0
                    choice = random.randint(1,3)
                    if choice == 1:
                        if inbounds(self.pos, 0, ASSAULT_IMG_HEIGHT[self.state])[0]:
                            self.ready_shoot()       
                    elif choice == 2:
                        self.walk(enemy_direction(self.pos, player.pos))
                    else:
                        self.strafe(enemy_elevation(self.pos, player.pos))


            if self.state == 'shoot_right' or self.state == 'shoot_left': # if player is shooting left or right
                self.time +=0.1
                if round(self.time, 1) == 1.0 or round(self.time, 1) == 3.0 or round(self.time, 1) == 5.0:
                    ar_sound.rewind()
                    ar_sound.play()
                    self.shoot()
                if int(self.time) == ASSAULT_ROWS[self.state]*ASSAULT_COLS[self.state]:
                    self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                    self.time = 0
                    self.stuck = False
         
        if not self.alive:
            self.stuck = True
            self.shooting = False
            if int(self.time) == ASSAULT_ROWS[self.state]*ASSAULT_COLS[self.state]-1:
                pass
                #is dead, keep body on screen
            else:
                self.time+=0.1
             
            
class Defender:
    def __init__(self, image, position, velocity, direction):
        self.type = 'bot'
        self.p_image = image
        self.state = 'walk_left' #which animation to use
        self.image = image[self.state]
        self.pos = position
        self.vel = velocity
        self.time = 0
        self.action_time = 0
        self.stuck = False # if the character can preform any other animations
        self.direction = direction # last known direction that the character faced
        self.dodge = False
        
        self.width = DEFENDER_IMG_WIDTH[self.state]
        self.height = DEFENDER_IMG_HEIGHT[self.state]
        
        self.health = defender_health
        self.attack = defender_attack
        self.alive = True
        
    def damage(self, damage):
        if self.health >= 1:
            self.health-=damage
            img = blood_image['blood_right'] if self.direction == 'right' else blood_image['blood_left']
            blood_effect = Blood(self.pos, img, ('blood_right' if self.direction == 'right' else 'blood_left'))
            blood.append(blood_effect)
        if self.alive and self.health <= 0:
            self.alive = False
            self.stuck = True
            self.time = 0
            self.vel =[0,0]
            self.vel = [0,0]
            self.state = 'death_right' if self.direction == 'right' else 'death_left'
            self.dodge = True
    
    def ready_shoot(self):
        self.stuck = True
        self.shooting = True
        self.time = 0 # reset time
        self.vel = [0,0] # stop moving
        self.state = 'shoot_right' if self.direction == 'right' else 'shoot_left' # choose which animation to use based on last direction 
        
    def shoot(self): #multiple bullets are spawned to imitate shotgun blast
        if self.direction == 'right': #multiple bullets because shotgun
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED,0], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED,0.25*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED, -0.25*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED,0.5*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED, -0.5*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
        else:
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED,0], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED,0.25*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED, -0.25*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED,0.5*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
            
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED, -0.5*BULLET_SPEED], bullet_image, self.type, self.attack)
            bullets.append(bullet)
        
    def walk(self, direction):
        distance = abs(player.pos[0]-self.pos[0])
        if direction == 'left' and distance >= engagement_distance:
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = -BOT_SPEED
            return
        elif direction == 'left':
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = BOT_SPEED
        if direction == 'right' and distance >= engagement_distance:
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = BOT_SPEED
        elif direction == 'right':
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = -BOT_SPEED
            
    def strafe(self, elevation):
        move = random.randint(1,10)
        if elevation == 'up':
            if move == 10:
                self.vel[1] = -BOT_SPEED
            else:    
                self.vel[1] = BOT_SPEED
            
        elif elevation == 'down':
            if move == 10:
                self.vel[1] = BOT_SPEED
            else:    
                self.vel[1] = -BOT_SPEED

        
    def draw(self, canvas):
        col = int(self.time)%DEFENDER_COLS[self.state]
        row = int(self.time)//DEFENDER_COLS[self.state]
        center_x = DEFENDER_IMG_WIDTH[self.state]/2+ col*DEFENDER_IMG_WIDTH[self.state]
        center_y = DEFENDER_IMG_HEIGHT[self.state]/2 +row*DEFENDER_IMG_HEIGHT[self.state]
        canvas.draw_image(self.image, 
                          (center_x, center_y),
                          (DEFENDER_IMG_WIDTH[self.state], DEFENDER_IMG_HEIGHT[self.state]), 
                          self.pos, 
                          PLAYER_SIZE)
    def update(self):
        global image
        self.image = self.p_image[self.state]
        
        next_pos = [self.pos[0] + self.vel[0], self.pos[1] + self.vel[1]]        
        wall_collision_x = False
        wall_collision_y = False
        
        if self.alive and inmap(self.pos, DEFENDER_IMG_WIDTH[self.state], DEFENDER_IMG_HEIGHT[self.state])[0]:
        
            for wall in walls:
                if wall.collide(next_pos, DEFENDER_IMG_WIDTH[self.state], DEFENDER_IMG_HEIGHT[self.state])[0]:
                    wall_collision_x = True
                if wall.collide(next_pos, DEFENDER_IMG_WIDTH[self.state], DEFENDER_IMG_HEIGHT[self.state])[1]:
                    wall_collision_y = True

            if not wall_collision_x and inmap(next_pos, DEFENDER_IMG_WIDTH[self.state], DEFENDER_IMG_HEIGHT[self.state])[0]:
                #update the x position on the x velocity
                self.pos[0] += self.vel[0]
            if not wall_collision_y and inmap(next_pos, DEFENDER_IMG_WIDTH[self.state], DEFENDER_IMG_HEIGHT[self.state])[1]:    
                #update the y position
                self.pos[1] += self.vel[1]       

            if self.vel != [0, 0] and self.alive:
                self.time+=0.1 
                if int(self.time) == DEFENDER_ROWS[self.state]*DEFENDER_COLS[self.state] or (abs(self.pos[1]-player.pos[1]) <= 6 and self.vel[0] == 0):
                    self.vel = [0,0]
                    self.time = 0

            elif not self.stuck and self.alive:
                self.action_time+=0.1
                self.direction = enemy_direction(self.pos, player.pos)
                self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                if int(self.action_time) >= 1:
                    self.action_time = 0
                    choice = random.randint(1,3)
                    if choice == 1:
                        if inbounds(self.pos, 0, DEFENDER_IMG_HEIGHT[self.state])[0]:
                            self.ready_shoot()        
                    elif choice == 2:
                        self.walk(enemy_direction(self.pos, player.pos))
                    else:
                        self.strafe(enemy_elevation(self.pos, player.pos))


            if self.state == 'shoot_right' or self.state == 'shoot_left': # if player is shooting left or right
                self.time +=0.1
                if round(self.time, 1) == 0.5:
                    shotgun_sound.rewind()
                    shotgun_sound.play()
                if round(self.time, 1) == 2.0:
                    self.shoot()
                if int(self.time) == DEFENDER_ROWS[self.state]*DEFENDER_COLS[self.state]:
                    self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                    self.time = 0
                    self.stuck = False

        if not self.alive:
            self.stuck = True
            self.shooting = False
            if int(self.time) == DEFENDER_ROWS[self.state]*DEFENDER_COLS[self.state]-1:
                pass
                #is dead, keep body on screen
            else:
                self.time+=0.1

    
class Scout:
    def __init__(self, image, position, velocity, direction):
        self.type = 'bot'
        self.p_image = image
        self.state = 'walk_left' #which animation to use
        self.image = image[self.state]
        self.pos = position
        self.vel = velocity
        self.time = 0
        self.action_time = 0
        self.stuck = False # if the character can preform any other animations
        self.direction = direction # last known direction that the character faced
        self.dodge = False
        
        self.width = SCOUT_IMG_WIDTH[self.state]
        self.height = SCOUT_IMG_HEIGHT[self.state]
        
        self.health = scout_health
        self.attack = scout_attack
        self.alive = True
        
    def damage(self, damage):
        if self.health >= 1:
            self.health-=damage
            img = blood_image['blood_right'] if self.direction == 'right' else blood_image['blood_left']
            blood_effect = Blood(self.pos, img, ('blood_right' if self.direction == 'right' else 'blood_left'))
            blood.append(blood_effect)
        if self.alive and self.health <= 0:
            self.alive = False
            self.stuck = True
            self.time = 0
            self.vel =[0,0]
            self.vel = [0,0]
            self.state = 'death_right' if self.direction == 'right' else 'death_left'
            self.dodge = True
    
    def ready_shoot(self):
        self.stuck = True
        self.shooting = True
        self.time = 0 # reset time
        self.vel = [0,0] # stop moving
        self.state = 'shoot_right' if self.direction == 'right' else 'shoot_left' # choose which animation to use based on last direction 
        
    def shoot(self):
        if self.direction == 'right': #multiple bullets because shotgun
            bullet_pos = [self.pos[0]+PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[BULLET_SPEED,(random.randint(-scout_inaccuracy,scout_inaccuracy)/10)], bullet_image, self.type, self.attack)
            bullets.append(bullet) 
        else:
            bullet_pos = [self.pos[0]-PLAYER_SIZE[0]/2, self.pos[1]-64]
            bullet = Bullet(bullet_pos,[-BULLET_SPEED,(random.randint(-scout_inaccuracy,scout_inaccuracy)/10)], bullet_image, self.type, self.attack)
            bullets.append(bullet)
        
    def walk(self, direction):
        distance = abs(player.pos[0]-self.pos[0])
        if direction == 'left' and distance >= engagement_distance:
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = -BOT_SPEED
            return
        elif direction == 'left':
            self.state = 'walk_left'
            self.direction = 'left'
            self.vel[0] = BOT_SPEED
        if direction == 'right' and distance >= engagement_distance:
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = BOT_SPEED
        elif direction == 'right':
            self.state = 'walk_right'
            self.direction = 'right'
            self.vel[0] = -BOT_SPEED
            
    def strafe(self, elevation):
        move = random.randint(1,10)
        if elevation == 'up':
            if move == 10:
                self.vel[1] = -BOT_SPEED
            else:    
                self.vel[1] = BOT_SPEED
            
        elif elevation == 'down':
            if move == 10:
                self.vel[1] = BOT_SPEED
            else:    
                self.vel[1] = -BOT_SPEED

        
    def draw(self, canvas):
        col = int(self.time)%SCOUT_COLS[self.state]
        row = int(self.time)//SCOUT_COLS[self.state]
        center_x = SCOUT_IMG_WIDTH[self.state]/2+ col*SCOUT_IMG_WIDTH[self.state]
        center_y = SCOUT_IMG_HEIGHT[self.state]/2 +row*SCOUT_IMG_HEIGHT[self.state]
        canvas.draw_image(self.image, 
                          (center_x, center_y),
                          (SCOUT_IMG_WIDTH[self.state], SCOUT_IMG_HEIGHT[self.state]), 
                          self.pos, 
                          PLAYER_SIZE)
    def update(self):
        global image
        self.image = self.p_image[self.state]
        
        next_pos = [self.pos[0] + self.vel[0], self.pos[1] + self.vel[1]]        
        wall_collision_x = False
        wall_collision_y = False
        
        if self.alive and inmap(self.pos, SCOUT_IMG_WIDTH[self.state], SCOUT_IMG_HEIGHT[self.state])[0]:
        
            for wall in walls:
                if wall.collide(next_pos, SCOUT_IMG_WIDTH[self.state], SCOUT_IMG_HEIGHT[self.state])[0]:
                    wall_collision_x = True
                if wall.collide(next_pos, SCOUT_IMG_WIDTH[self.state], SCOUT_IMG_HEIGHT[self.state])[1]:
                    wall_collision_y = True

            if not wall_collision_x and inmap(next_pos, SCOUT_IMG_WIDTH[self.state], SCOUT_IMG_HEIGHT[self.state])[0]:
                #update the x position on the x velocity
                self.pos[0] += self.vel[0]
            if not wall_collision_y and inmap(next_pos, SCOUT_IMG_WIDTH[self.state], SCOUT_IMG_HEIGHT[self.state])[1]:    
                #update the y position
                self.pos[1] += self.vel[1]       

            if self.vel != [0, 0] and self.alive:
                self.time+=0.1 
                if int(self.time) == SCOUT_ROWS[self.state]*SCOUT_COLS[self.state] or (abs(self.pos[1]-player.pos[1]) <= 6 and self.vel[0] == 0):
                    self.vel = [0,0]
                    self.time = 0

            elif not self.stuck and self.alive:
                self.action_time+=0.1
                self.direction = enemy_direction(self.pos, player.pos)
                self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                if int(self.action_time) >= 1:
                    self.action_time = 0
                    choice = random.randint(1,3)
                    if choice == 1:
                        if inbounds(self.pos, 0, SCOUT_IMG_HEIGHT[self.state])[0]:
                            self.ready_shoot()         
                    elif choice == 2:
                        self.walk(enemy_direction(self.pos, player.pos))
                    else:
                        self.strafe(enemy_elevation(self.pos, player.pos))


            if self.state == 'shoot_right' or self.state == 'shoot_left': # if player is shooting left or right
                self.time +=0.1
                if round(self.time, 1) == 2.0:
                    pistol_sound.rewind()
                    pistol_sound.play()
                    self.shoot()
                if int(self.time) == SCOUT_ROWS[self.state]*SCOUT_COLS[self.state]:
                    self.state = 'walk_right' if self.direction == 'right' else 'walk_left'
                    self.time = 0
                    self.stuck = False

        if not self.alive:
            self.stuck = True
            self.shooting = False
            if int(self.time) == SCOUT_ROWS[self.state]*SCOUT_COLS[self.state]-1:
                pass
                #is dead, keep body on screen
            else:
                self.time+=0.1
    
# Handler to draw on canvas
def draw(canvas):
    global player, deathoverlay, transferoverlay, death, overlays, credit
    #draw background
    canvas.draw_image(bgrd_image[current_background],(BGRD_WIDTH[current_background]/2,BGRD_HEIGHT[current_background]/2),(BGRD_WIDTH[current_background], BGRD_HEIGHT[current_background]), background_pos,(BGRD_WIDTH[current_background],BGRD_HEIGHT[current_background]))
    if menu:
        if credit:# do the special thanks to jaden
            credit = False
            jadencredit = CreditOverlay((WIDTH/2,HEIGHT/2), credit_image)
            overlays.append(jadencredit)
        else:
            #draw the background
            canvas.draw_image(menu_image,(WIDTH/2,HEIGHT/2),(WIDTH, HEIGHT), [WIDTH/2,HEIGHT/2],(WIDTH,HEIGHT))
            #do the cool background scroll thing
            bgrd_move()   
            bgrd_sound.play()
            if transferoverlay.state:
                if transferoverlay.switch:
                    new_game()
                    transferoverlay.switch = False
    elif not player.alive and not death:
        #do the death overlay
        death = True
        deathoverlay = DeathOverlay(death_pos, death_image)
        overlays.append(deathoverlay)
        deathoverlay.state = True
    
    #update all the objecys/overlays
    objects.sort(key=object_y)
    for o in objects:
        o.draw(canvas)
        o.update()
    
    for b in bullets:
        if not inbounds(b.pos, BULLET_IMG_WIDTH, BULLET_IMG_HEIGHT)[0] or not inbounds(b.pos, BULLET_IMG_WIDTH, BULLET_IMG_HEIGHT)[1]:
            bullets.remove(b)
        b.draw(canvas)
        b.update()
    for w in walls:
        w.draw(canvas)
    for b in blood:
        b.draw(canvas)
        b.update()
    for o in overlays:
        o.draw(canvas)
        o.update()


def key_press(key):
    global menu, transferoverlay, deathoverlay, overlay, bullets, blood, walls, objects, death, dialogueoverlay, dialogue
    if not menu and player.alive: 
        #you cant do anything while stuck duh
        if player.stuck:
            pass
        else:
            #shooting 
            if key == simplegui.KEY_MAP['A']:
                if player.ammo > 0:
                    player.stuck = True
                    player.shooting = True
                    player.stop = False
                    player.time = 0 # reset time
                    player.vel[0], player.vel[1] = 0,0 # stop moving
                    player.state = 'shoot_right' if player.direction == 'right' else 'shoot_left' # choose which animation to use based on last direction
                else:
                    empty_sound.rewind()
                    empty_sound.play()

            #rolls
            if key == simplegui.KEY_MAP['S']:
                player.roll()

            #reload/ check mags
            if key == simplegui.KEY_MAP['R']:
                if player.magazines > 0:
                    player.reload()

            if key == simplegui.KEY_MAP['T']:
                player.check()

            #basic movement
            if key == simplegui.KEY_MAP['right']:
                player.direction = 'right'
                player.vel[0] = PLAYER_SPEED
                player.state = 'walk_right'
            if key == simplegui.KEY_MAP['left']:
                player.direction = 'left'
                player.vel[0] = -PLAYER_SPEED
                player.state = 'walk_left'
            if key == simplegui.KEY_MAP['down']:
                player.vel[1] = PLAYER_SPEED
            if key == simplegui.KEY_MAP['up']:
                player.vel[1] = -PLAYER_SPEED
            
            #dialogue
            #dialogue is based of of which frame of spritesheet to use
            if dialogue:
                if key == simplegui.KEY_MAP['space']:
                    click_sound.rewind()
                    click_sound.play()
                    dialogueoverlay.state+=1
                    dialogueoverlay.amount-=1
                    if dialogueoverlay.amount == 0:
                        dialogue = False
                    #ammo from jaegers stash, special event
                    if dialogueoverlay.state == 6:
                        player.magazines+=25
                    #boss conversation dialogue
                    elif dialogueoverlay.state == 16:
                        ak_sound.rewind()
                        ak_sound.play()
                    #beat the game dialogue
                    elif dialogueoverlay.state == 20:
                        reset()
    else:
        if key == simplegui.KEY_MAP['space']:
            if menu:
                #remove menu, start game
                click_sound.rewind()
                click_sound.play()
                transferoverlay.state = True
            elif death:
                #reset
                reset()


def key_release(key):
    if not menu:
        #basic movement
        if key == simplegui.KEY_MAP['A']:
            player.stop = True
        if not player.stuck:
            if key == simplegui.KEY_MAP['right']:
                player.vel[0] = 0
            elif key == simplegui.KEY_MAP['left']:
                player.vel[0] = 0
            elif key == simplegui.KEY_MAP['down']:
                player.vel[1] = 0
            elif key == simplegui.KEY_MAP['up']:
                player.vel[1] = 0

#begin a new session, credit for jaden only have menu and scrolling background
new_session()
    
# Create a frame and assign callbacks to event handlers
frame = simplegui.create_frame("Home", WIDTH, HEIGHT)
frame.set_draw_handler(draw)

#handle keys
frame.set_keydown_handler(key_press)
frame.set_keyup_handler(key_release)

frame.set_canvas_background("black")
# Start the frame animation
frame.start()
