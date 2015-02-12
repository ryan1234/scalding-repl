# Scalding REPL (in Docker)

I'm sure something like this exists already, but I couldn't find it.

Goal was to make the barrier to entry really low for developers looking to get going with Scalding via the REPL.

# Starting a Container
1. `docker pull ryan1234/scalding-repl`  
2. `docker run -it -v /home/scala-repl:/src --rm ryan1234:scalding`  

# Notes
1. (--rm) The container will remove itself after you're done using the REPL. (Control-D to exit)  
2. (-v /home/scala-repl:/src) Mapping a local file location (/home/scala-repl) to the /src directory in the container. I like to edit files and load them in the REPL for quick testing.  
3. In the REPL, load a file with `:load /src/<filename>.scala`  

# Todo 
My examples tend to need a larger Java heap than the defaults, so I plan to make the heap size tunable with ENV parameters.
