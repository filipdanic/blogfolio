---
title: How to Use Option (Alt) + Arrows To Navigate Between Words in iTerm2
seo_description: A quick guide on how to use Alt + left arrow and Alt + right arrow to move between words with iTerm2. Or rather backward-word and forward-word.
promo_photo: /content/images/2018/iterm2_option_keyescape_chars.png
date: 2018-08-30
tags:
---

I’ll be honest, I’m not much of a terminal power user. I use iTerm2 as my terminal emulator and there are some things I like to customize. And it bugs me how cumbersome it is to enable the ability to switch between words with <kbd>⌥</kbd> + <kbd>←</kbd> and <kbd>⌥</kbd> + <kbd>→</kbd>.

Apparently, this is actually called _backward-word_ and _forward-word._ You can see your current setup with:

```bash
bindkey -L | grep backward-word
```

And:

```bash
bindkey -L | grep forward-word
```

<figure class="blog-post-image"><img src="/content/images/2018/keybinds_backward_word_forward_word.png" alt="Sample output of running the previous command." /><figcaption>Sample output.</figcaption></figure>

You might even like the defaults. (I doubt it.) Now, you can manually set the binding keys via the terminal of course, but I don’t really get how it’s used and I hate typing out character codes by hand. 🙂

So instead, I’m going to document this method that uses the iTerm2 preferences menu – for future reference to myself and to others who might have the same problem. (Please note that this is specific to this emulator.)

## How to Configure backward-word and forward-word in iTerm2

First, in iTerm2, go to **Preferences > Profile > Keys**.

Here you need to set your left <kbd>⌥</kbd> key to act as an _escape character._ Or _Esc+_ as it is written. (See screenshot.)

<figure class="blog-post-image"><img src="/content/images/2018/iterm2_option_keyescape_chars.png" alt="Left Option Key Settings" /><figcaption>Left Option Key Settings</figcaption></figure>

Then, in your **Key Mappings** on the same screen, we need to redefine the shortcuts for our desired combination.

<figure class="blog-post-image"><img src="/content/images/2018/iterm2-key-mappings.png" alt="Screenshot of Key Mappings Section" /><figcaption>Screenshot of Key Mappings Section</figcaption></figure>

Find the current shortcut for <kbd>⌥</kbd> + <kbd>←</kbd> (or create a new one), with the following settings:

- _Action:_ **Send Escape Sequence**
- _Esc +:_ <kbd>b</kbd>

<figure class="blog-post-image"><img src="/content/images/2018/iterm2_backward_word.png" alt="Configure backward-word" /><figcaption>Configure backward-word</figcaption></figure>

Find or create a shortcut for <kbd>⌥</kbd> + <kbd>→</kbd> as well with:

- _Action:_ **Send Escape Sequence**
- _Esc +:_ <kbd>f</kbd>

<figure class="blog-post-image"><img src="/content/images/2018/iterm2_forward_word.png" alt="Configure backward-word" /><figcaption>Configure forward-word</figcaption></figure>

And that’s it, happy hacking! 🎉 If you end up having a lot of these presets, it would be a good idea to export and save them somewhere for future use.
