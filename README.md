# Tmux usage
In tmux, every terminal is called panel

#### split horizontally
<pre>
1. press Key <b>ctrl</b> + <b>b</b>
2. press Key <b>shift</b> + <b>"</b>
</pre>

#### split vertically
<pre>
1. press Key <b>ctrl</b> + <b>b</b>
2. press Key <b>shift</b> + <b>%</b>
</pre>

#### To move from one pane to another, simply use the prefix followed by the arrow key:
<pre>
1. press Key <b>ctrl</b> + <b>b</b>
2. press <b>[arrow key]</b>
</pre>


#### Resizing Panes
Lets say we need a little extra breathing room for one of our panes, and want to expand the pane down a few lines. For this, we will go into the tmux prompt:
ctrl+b :
From there we can type resize-pane followed by a direction flag: -U for up, -D for down -L for left and -R for right. The last part is the number of lines to move it over by.
As an example, if we are in the top pane and want to expand it down by 2 lines, we would do the following:
ctrl+b :
resize-pane -D 2

<pre>
1. press Key <b>ctrl</b> + <b>b</b>
2. press Key <b>shift</b> + <b>:</b>
3. input <b>resize-pane -D 2</b>  will move pane 2 lines down, other flags -U, -L, -R similarly.
</pre>


#### Customize themes
edit tmux.conf 
```
$ vi ~/tmux.conf
```
and then source it with tmux source-file ~/.tmux.conf.
```
$ tmux source-file ~/.tmux.conf
```

#### list of primary commands
1. Start new named session:
```$ tmux new -s [session name]```

2. Detach from session:
```$ ctrl+b d```

3. List sessions:
```$ tmux ls```

4. Attach to named session:
```$ tmux a -t [name of session]```

5. Kill named session
```$ tmux kill-session -t [name of session]```

6. split panes horizontally:
```$ ctrl+b "```

7. Split panes vertically:
```$ ctrl+b %```

8. Kill current pane:
```$ ctrl+b x```

9. Move to another pane:
```$ ctrl+b [arrow key]```

10. Kill tmux server, along with all sessions:
```$ tmux kill-server```

https://hackernoon.com/a-gentle-introduction-to-tmux-8d784c404340
