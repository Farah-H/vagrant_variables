# Environment Variables

These exist globally on a speciific environment. Generally you don't want to have too many of them. And you can interpolate them into code and other services. 

## Agenda
- What are vairables vs Environment variable in Basg 
- Process and child process
    ![](https://media.discordapp.net/attachments/770295530336288770/781175595642912768/unknown.png)
- default variables 
- How to set the enironment variables in bash 


```bash
MY_VAR=hello
echo $MY_VAR
>hello
DIR=$(pwd)
echo $DIR
```

These variables are *not environment variables* and exist only in the current process (the current terminal). Once you restart the terminal these variables do not continue. 

## Child Process 
WHen your terminal runs another file or bash script it makes a child process. A child process is basically a new terminal. 

## Export 

You can use export to make a variable available to the child process:

```bash
MY_VAR=hello
export MY_VAR
./my_process.sh
> This is a line from my process
> hello
```

This is still not permanent, when you restart your terminal, it will be lost. 

## Making variable persistent in your computer
- The definitive response lies in understanding how terminals are created 
- the PATH taken
- Each individual terminal has a path to conclude before opening for you to type
- To set an environmennt variable  you are going to write in one of the files that it reads as it does its path. 


__You want to have this in .profile:__
```bash
#if running bash
if [-n "$BASH_VERSION" ]; then
    # include .bashhrc if it exists
    if [-f "$HOME/.bashrc ]; then
    "$HOME/.bashrc"
    fi
fi
```

## Concluding
we covered:
- variables VS local variables
- how variables run in scrip & child process
- how to create environment variables from variables
- how to make persistent variables that last between logons. 