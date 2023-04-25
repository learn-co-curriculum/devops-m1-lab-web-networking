# Web Networking Lab

## Task

In this lab, we'll take a look at web networking in an interactive fashion using the `ping`, `traceroute` and `curl` commands.

## Instructions

### Testing network connectivity with `ping`

Go ahead and log into a session on your Ubuntu VM. You can `ping` with any remote host, but for the purposes of this lab let's try connecting to Google:

```bash
$ ping www.google.com
```

Take a moment to analyze the output of the ping command. Pinging can be stopped by pressing `<Ctrl-c>`.

`ping` is generally useful for troubleshooting times when either the host or remote server are not working, and you want to see if the endpoint is even accessible in the first place. For instance, let's say you have trouble connecting to `google.com` on your browser; you can try pinging Google, or any other random websites to find out if it's an issue with your local connection or the actual server you're connecting to. Likewise, you can also gather information like how distant a certain endpoint is by how long the travel time is.

Take a screenshot of the output before we move on to the next step.

### Tracing Network Path with `traceroute`

For this next step, we're going to have to install the `traceroute` tool since it is not available with *Ubuntu* out of the box. This can be achieved with `apt`:

```bash
$ sudo apt install traceroute
```

If the terminal prompts you for credentials, go ahead and provide your password. Once the package finishes installing, run the following command:

```bash
$ traceroute www.google.com
```

Note how the results printed to the screen show us the hops that were taken on the network to get from our client to the host. If traceroute has not finished executing yet, end it my pressing `Ctrl+C`.

Take a screenshot of this output, then move on to the final step.

### Retrieving Web Content with `curl`

Another type of information we can retrieve from the internet using our terminal is web content. This is facilitated using the `curl` command. As output, we will be receiving the HTML content of the website. Run the following in your terminal:

```bash
$ curl www.google.com
```

Though overwhelming at first, we can see that there is HTML, CSS and more printed to the screen. For the purpose of submission, save the output of this `curl` command into a text file and upload it as part of your submission. Using knowledge from the prior lab, constructing the following statement provides what we need:

```bash
$ curl www.google.com > output.txt
```

Let's view the contents of the output file:

```bash
$ cat output.txt
```

## Submission

Submit the screenshots of the terminal output for the `ping` and `traceroute` commands, as well as the "output.txt" file you filled with the `curl` results.

