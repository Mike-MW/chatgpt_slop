You must make sure your OpenAI account has at least $5 on it to use this. This is not the same as having a subscription to ChatGPT, you must go to https://platform.openai.com/settings/organization/billing/overview and add a credit balance there to use it or you'll get a "quota limit" error.

Edit the config to include the following:

your openai api key

global listen is whether or not you want to be able to activate it from another window or not

device is the system name of your microphone

backend is set to gel with linus by default but switch it to dshow if you use windows

keycode is the code of the key you want to activate the recording, if you want a keycode that's not part of the standard keyboard and you have a keyboard/mouse with macro keys you could use 124 - 135 for F13-F24

The prompt can be multi-lined but only if you have """ before and """ after the prompt.

You can increase or decrease the message limit to determine how much info chat gpt stores in memory during your conversation.

Once you have config sorted save and close it, then open a terminal window by right clicking in the folder, click terminal, then type in "cargo run" and hit enter, it will compile the files, you can then test it to make sure it's working

When finished you can CTRL+C to exit, it will show an error when yo do so but don't worry about it.

You can then run "cargo build --release" in the terminal to build a release version inside the "target" folder with an EXE that takes you straight to the listening part, but before you use it you must copy the config toml file into the release folder
