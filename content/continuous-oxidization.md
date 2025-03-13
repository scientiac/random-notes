+++
title = "Continuous: Oxidization"
date = 2025-03-12T22:33:37+05:45
[taxonomies] 
tags = ["articles"]
+++

This is not the first time this has happened. I am trying to replace all the programs I use
to the ones written in rust. Why? You might ask. [_It's for fun!_] I get to rice new things.
Rust is a cool kid language, but unlike other cool kids it's a sophisticated one too. So, it's
no doubt that it's going to rule the world, maybe not for the next 100 years, but I could bet 50.
Now, let's come straight to the programs I used to use and the ones I have replaced with.

> ### _'hyprland' with 'niri'_  
>
> Unlike hyprland niri is not exactly a tiling window manager but a scrolling one. It's a cool
> concept where my existing window's don't get resized when I open a new one, it just adds itself
> to it's side like a photo reel. [_No, not instagram._]
***

> ### _'waybar' with 'way-edges'_  
>
> way-edges is not a bar but it can act like one and since I like no distractions on my workspace
> they[_(It has multiple widgets.)_] hide automatically and show up on hover. I just love it.
***

> ### _'ghostty' with 'alacritty'_  
>
> This feels like a step-down because ghostty is feature rich whereas alacritty is minimal. Let's see
> how this one goes. I rarely use the image rendering feature and alacritty does great with everything text.
***

> ### _'zsh' with 'nushell'_  
>
> There were two shells to choose from, one was fish and another was nu, I went with the cool kid in the block but
> let's see how it holds up. It feels more stable and super intuiative than I last tried it.
***

> ### _'fzf' with 'skim'_  
>
> I used fzf but skim was almost a drop in replacement for it. I say "almost" because some arguments that fzf
> supported didn't work on skim. [_Well, they were cosmetic arguments so who cares._]

# Now we are heading Deeper into the Iceberg

- ___'grep' with 'ripgrep'___ : _`ripgrep` is just faster than `grep`._  
- ___'ls' with 'eza/nu'___ : _I do have `zsh` as a fallback shell, and I would use `eza` there, otherwise `nu` handles `ls`   like a charm._
- ___'cd' with 'zoxide'___ : _Instead of walking through the dirs using `cd` I jump straight to where I want with `zoxide`._  
- ___'cat' with 'bat'___ : _Conbatination? Haha, it syntax highlights too._  
- ___'find' with 'fd'___ : _What is there "in" `fd` that isn't there `in` find._  
- ___'magic-wormhole' with 'magic-wormhole-rs'___ : _I am lying, I used the rs version all along._  
- ___'top/htop' with 'bottom'___ : _It just looks cool._  
- ___'dunst' with 'swayOSD'___ : _Dunst wasn't meant to be used as an OSD._  
- ___'trash-cli' with 'trashy'___ : _Well, I'll let my trash rust in the bin._ [_2025-03-13_]
- ___'coreutils' with 'uutils-coreutils'___ : _Well, since I am using everything else rust and bleeding edge, why not the core utilities too._ [_2025-03-13_]

# Things that Still Remain

- ___Terminal Multiplexer___ : I still have `tmux`. There exists `zellij`, but I rarely use this program.
- ___Notification Daemon___ : I use `mako`, and I don't know any that's written in rust and works on wayland.
- ___Launcher/Menu___ : Using `wofi`, and I don't know any that's written in rust and works on wayland.
- ___Git TUI___ : I am not go-ing away from lazygit.
- ___Screen Locker___ : Swaylock just looks cool, there is one locker in rust, but it looks boring. [_than swaylock_]

# Things that I am not Ready for

- ___Browser___ : Firefox
- ___Video Player___ : mpv
- ___Pdf Reader___ : sioyek
- ___Email Client___ : Thunderbird
- ___Music___ : Spotify

> I will be updating this as I go. No part 2 for this. It's Continuous Oxidization.
