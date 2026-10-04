# 🌈 Save the Unicorns — js13k Postmortem (Summary, for the long version scroll down)

*Save the Unicorns* is a story-based, "Undertale / Papers, Please!" inspired game made for js13kGames 2026, my first game jam ever✨. Unicorns have been expelled from the land by victorious horses, and you play a white horse who sells hats and helps them disguise themselves to escape the borders safely.

I started two weeks late (28 Aug instead of 13 Aug), so I submitted an incomplete but fully playable game.

## How It's Built🔨
- Dropped Kontra, since the game is just includes clicking, dialogue, and backgrounds (doesn't require complex methods/code).
- Images were shrunk to 80 x 45 pixels, reduced to a 3-color palette (plus a colored background), cleaned of noise in MS Paint, and converted to matrices which is displayed on the screen as colored pixels.
- Cutscenes, like the town scene and the unicorn silhouette, are also made up of matrices.
- Used Claude for ideas and code, and Antigravity for the dialogue box and disguise UI. I use AI moderately, I don't use it for generating art/photos/videos. and I'm not telling anyone to do the same.
- Used browser alerts instead of in-game alerts to save space.

## What Went Well✅
- I'm happy with how the game looks.
- The story/text fit into the game.
- It was functional and playable.

## What Went Wrong
- The text was too small on mobile, which I never tested.
- A story-based game is very hard to keep under 13KB.
- I started too late.
- Many mechanics were cut: the day/night system, inventory, save/load, purchasing, the audio, and the rainbow escape on the last day.

## Takeaway🌸
I'm glad I took part in this game jam and made a game under 13KB. Thanks to everyone who made the jam happen, to @end3r on Discord for helping and answering my questions, and to everyone who played and left feedback.

# 🔴🟠🟡🟢🔵🟣Save the Unicorns — js13k Postmortem🌈 (Original)

This postmortem is more like a diary than a technical document. I'm writing about my thoughts and experience. I hope that whoever reads it enjoys it.

## The Prologue (I guess?)

I'm writing this on the 3rd of October 2026:

Hi! I never found a job that fits my degree, and I stayed unemployed for too long. I have some experience making games using Unity and Godot, so I decided to join game jams to try and win prizes, maybe build a portfolio out of it, or at least get some experience and maybe start my own game jams.

So I joined around 3 game jams. The first one is this game jam (js13kGames 2026). The second one is still in the voting stage (it ended around 1–2 weeks after the js13k submission deadline). The third one I'm still working on, and I have a month to submit it.

So js13k is my first game jam EVER!🌸

I started the game jam late (I was two weeks late). If I had known how complex the challenge actually is, I would've started earlier. Because of my late start, I submitted my game incomplete. It was completely functional, but there were core ideas that had to be dropped because of my bad planning.

## The Idea💡

I was binge-watching *Undertale* gameplay for around a week, so I guess I brainwashed myself into making an Undertale-inspired game (lol). I thought of another idea where I would make a unicorn pastry/milkshake shop, but I felt like it wasn't unique enough, and I loved my first idea, so I stuck to it.

I thought of unicorns and horses as two races. A war started between them, and the victorious horses kicked the unicorns out of the land. I made the unicorns the expelled ones, and they have to disguise themselves to leave the borders safely. (Reversing the roles would be boring, because the horses would all just disguise as unicorns: white coat and colorful mane. Versus disguising unicorns as horses, where there are lots of horse breeds, which adds variety to the disguise options.)

The "escaping the borders" part was inspired by *Papers, Please!*. It isn't a direct copy of its gameplay. The objective of my game is helping as many unicorns as possible leave safely and go back to their kingdom with their kind.

## How It's Built💻

First of all, I did a little bit of research to know how to start. I read about Kontra and made a demo/mini game using it. But then I realized that I might not need it at all, because my game is story-based and there aren't lots of elements: just background images (not really images, I'll explain later), dialogues, and the only input is clicking. So I decided not to use Kontra and to just minimize the code when I'm done with the game.

### AI Usage🤖

I was using Claude to organize my ideas and help me with coding. (I know AI is bad, and I hate AI-generated photos/videos, but I believe in moderate usage of AI. I feel like if I don't keep up with a certain technology, I will be left behind while others use it to help/automate lots of things. I'm NOT trying to convince anyone to use AI. I'm just sharing what I feel about it.)

### The Gameplay🎮

My original idea included a day/night system. In the day you scavenge, then buy from the shop, then a cutscene plays, then the unicorn disguise gameplay begins. At night you are shown the results of the day (did they escape and survive or not). This also means there should be an inventory system, a save and load system, and a purchasing system (I guess). I decided to make the player a white horse that sells hats, so he is able to give the unicorns hats to disguise themselves.

🔴 *The images containing my original idea is in a folder named "idea" on this page.*

### Image to Matrix🖼️

I started to add the images for the intro and the cutscenes. I took some images, pixelated them, and resized them to 166 x 96 pixels. But then I realized that adding images would take too many kilobytes. So I asked Claude, and it suggested turning them into matrices and adding a color palette. Claude took the images and converted them to matrices. Initially the matrix size was 166 x 96, and the color palette contained around 8 colors. But again I asked Claude if shrinking the matrix size and reducing the colors would reduce the file size significantly, and it said yes. So I resized all the images to 80 x 45 pixels and reduced the palette to 3 colors. The fourth color (yellowish tan?) was added as a background to the scenes. I sent them to Claude to convert them into matrices, but they still took too much space. Then Claude said that reducing the noise in the images would reduce their size. So I opened the images in MS Paint and removed the random dots. For example this is an image before and after reduction(not converted to matrix yet):

<img width="166" height="96" alt="castle5" src="https://github.com/user-attachments/assets/7e91fdd0-846b-4dd9-87e8-8387e84aaa0a" />
<img width="80" height="45" alt="castle" src="https://github.com/user-attachments/assets/03681c8c-e36a-4b5e-b2a4-341767c957d9" />

### The Disguise Gameplay⭐

I ran out of credits in Claude, so I gave Antigravity a try. It was good, but the advanced models reset after a week. It generated the disguise gameplay UI and dialogue box (I made a drawing to explain to the AI how I wanted the gameplay UI to look, and it recreated it successfully). Then I ran out of credits there too and went back to Claude.

(Side note: Claude wastes lots of credits too, but I did two things to try and prevent that. 1. At the end of each prompt, I explicitly asked it not to waste my credits/quota/tokens. 2. After a certain number of questions, I open a new chat, send the latest version of my file, and start asking in the new chat. My theory is that everything in the chat is summarized and sent with my prompt, and that's why it was wasting my credits. Creating a new chat is my attempt to avoid that kind of overhead.)

<img width="740" height="108" alt="Screenshot 2026-10-03 180746" src="https://github.com/user-attachments/assets/7dd7afd0-4792-481b-8c12-31e711c60f70" />
<img width="956" height="392" alt="Screenshot 2026-10-03 175810" src="https://github.com/user-attachments/assets/5d95348e-8cc0-4820-94ca-e0576ddfba9c" />

### The Cutscenes🎞️

The in-game cutscenes were just an image matrix (town scene) and a silhouette of a unicorn, also created using a matrix, where dots (.) represent transparent pixels and numbers represent colored pixels. The dialogue box was created using Antigravity (as well as the disguise scene). I tweaked it a bit because the colors were strong.

### The Story / Audio / In-Game Alerts💭

The original story/text was longer than the final version. I didn't know that text can take so much space. There was some audio in the game, but due to the size of the file, I dropped it at the last minute. Also, I was planning on adding in-game alerts, but according to Claude, it would've taken more space, so I used browser alerts in hopes of making the file smaller.

## What Went Well✅

- I am really happy with the looks of the game, even though I had to reduce the size of the images, which affected how it looked.
- I fitted the story into the game, which I am really glad worked.
- The game was functional and playable, which I am very proud of.

## What Went Wrong / What I'd Do Differently

- The text was super small on mobile devices. I didn't know that people could play on mobile devices, so I never tested it on one.
- I didn't know that a story-based game would be so hard to keep under 13KB. (I'm glad that I didn't know, because if I had, I might have never made this kind of game!)
- I wish I had started earlier. The game jam was a month long, but I only started after two weeks.
- LOTS of game mechanics/audio were dropped due to the size of the files and the time restriction.
- There was a part that included a rainbow which the unicorns could walk over to escape on the last day, but I left it out for the same reason (time/file size).

## Takeaway✨
I'm so glad that I took part in this game jam, and I thank everyone who made it happen! Even if I don't get a really high score, I'm just happy to have had this experience, joined the challenge, and made a game under 13KB!

A special thanks to @end3r on Discord for helping me when I faced problems with my submission. He was very helpful. Thanks to everyone who participated, everyone who left feedback on my game, and everyone who tried it!

I hope I can be part of the next game jam. Good luck to everyone!
