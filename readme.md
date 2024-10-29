# Cursor Official instructions

# **Get Started**

## **Migrate from VS Code**

Cursor is a fork of VS Code. This allows us to focus on making the best way to code with AI, while offering a familiar text editing experience.

### [**](https://docs.cursor.com/get-started/migrate-from-vscode#import-extensions-themes-settings-and-keybindings)Import Extensions, Themes, Settings, and Keybindings**

You can import your VS Code configuration into Cursor with one-click. Navigate to **`Cursor Settings`** > **`General`** > **`Account`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/get-started/vscode-import.png

### [**](https://docs.cursor.com/get-started/migrate-from-vscode#staying-up-to-date)Staying Up to Date**

We periodically rebase Cursor onto the latest version of VS Code.

### [**](https://docs.cursor.com/get-started/migrate-from-vscode#why-not-an-extension)Why Not an Extension?**

As a standalone application, Cursor has more control over the UI of the editor, enabling greater AI integration. Some of our features, like Cursor Tab and CMD-K, are not possible as plugins to existing coding environments.

### [**](https://docs.cursor.com/get-started/migrate-from-vscode#settings)Settings**

You can open Cursor specific settings pane by clicking on the gear button top-right, by pressing **`Ctrl/⌘ + Shift + J`**, or with **`Ctrl/⌘ + Shift + P`** and typing **`Cursor Settings`**.

You can open VS Code specific settings with **`Ctrl/⌘ + Shift + P`**, and then typing **`VS Code Settings`**.

### [**](https://docs.cursor.com/get-started/migrate-from-vscode#why-is-the-activity-bar-in-cursor-horizontal)Why is the Activity Bar in Cursor horizontal?**

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/get-started/activity-bar.png

The activity bar is horizontal by default to save room for chat. If you prefer the normal vertical activity bar you can go to the VS Code settings and set **`workbench.activityBar.orientation`** to **`vertical`**, and restart Cursor.

## **Usage**

For more pricing info, please visit [**Cursor Pricing**](https://cursor.com/pricing).

### [**](https://docs.cursor.com/get-started/usage#subscription-tiers)Subscription Tiers**

Cursor offers multiple subscription tiers to fit your needs.

- **Hobby**
    - 14 days **Pro trial**
    - 50 slow **`premium`** model uses
    - 200 **`cursor-small`** uses
    - 2000 [**completions**](https://docs.cursor.com/tab/overview) uses
- **Pro**
    - 500 fast **`premium`** model uses per month
    - Unlimited slow **`premium`** model uses
    - Unlimited **`cursor-small`** uses
    - Unlimited [**completions**](https://docs.cursor.com/tab/overview) completions
    - 10 **`Claude Opus`** uses per month
- **Business**
    - Usage information is the same as the **`Pro`** tier
    - Extra benefits, detailed on the [**pricing page**](https://cursor.com/pricing)

### [**](https://docs.cursor.com/get-started/usage#premium-models)Premium models**

GPT-4, GPT-4o, and Claude 3.5 Sonnet are all counted as **`premium`** models.

### [**](https://docs.cursor.com/get-started/usage#pro-trial)Pro Trial**

All new users receive a 14-day Pro trial, granting access to all Pro features. After the 14-day period, users who have not upgraded will revert to the Hobby plan.

### [**](https://docs.cursor.com/get-started/usage#fast-and-slow-requests)Fast and Slow Requests**

By default, Cursor servers try to give all users fast **`premium`** model requests. However, during peak periods, users who run out of fast **`premium`** credits will be moved to a slow pool, which essentially is a queue of users waiting for a fast **`premium`** request to become available.

This queue is fair, and Cursor will do everything possible to keep the queue as short as possible. However, if you need more fast **`premium`** credits and don’t want to wait, you can add more requests on the [**settings page**](https://cursor.com/settings).

### [**](https://docs.cursor.com/get-started/usage#check-your-usage)Check Your Usage**

You can check your usage on the [**Cursor Settings**](https://cursor.com/settings) page. You can reach this page inside the Cursor application as well, under **`Cursor Settings`** > **`General`** > **`Account`**, and press “Manage Subscription” for pro users, or “Manage” for business users.

Cursor usage resets monthly, based on your subscription start date.

### [**](https://docs.cursor.com/get-started/usage#optional-usage-based-pricing)Optional Usage-based Pricing**

You may opt in to usage-based pricing for requests that go beyond what is included in your plan by visiting your [**settings page**](https://cursor.com/settings).

Usage-based pricing details:

- Usage-based pricing is per calendar month (not necessarily same as your billing cycle, will be billed roughly on the 2nd-3rd day of the month)
- If you immediately cancel a request or if it errors we do not count it
- You can configure a hard limit, and you will never ever have to pay more than the hard limit per month (for the usage-based pricing)
- Right now, usage-based pricing only applies to Claude 3 Opus and a few models in long context chat.

# Tab

## **Overview**

Cursor Tab is our native autocomplete feature. It’s a more powerful Copilot that suggests entire diffs with especially good memory.

Powered by a custom model, Cursor Tab can:

- Suggest edits around your cursor, not just insertions of additional code.
- Modify multiple lines at once.
- Make suggestions based on your recent changes and linter errors.

Free users receive 2000 suggestions at no cost. Pro and Business plans receive unlimited suggestions.

### [**](https://docs.cursor.com/tab/overview#ui)UI**

When Cursor is only adding additional text, completions will appear as grey text. If a suggestion modifies existing code, it will appear as a diff popup to the right of your current line.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cpp/ghost-text-example.png

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cpp/preview-box-example.png

You can accept a suggestion by pressing **`Tab`**, or reject it by pressing **`Esc`**. To partially accept a suggestion word-by-word, press **`Ctrl/⌘ →`**. To reject a suggestion, just keep typing, or use **`Escape`** to cancel/hide the suggestion.

Every keystroke or cursor movement, Cursor will attempt to make a suggestion based on your recent changes. However, Cursor will not always show a suggestion; sometimes the model has predicted that there’s no change to be made.

Cursor can make changes from one line above to two lines below your current line.

### [**](https://docs.cursor.com/tab/overview#toggling)Toggling**

To turn the feature on or off, hover over “Cursor Tab” icon on the status bar in the bottom right of the application.

## **Migrate from GitHub Copilot**

### [**](https://docs.cursor.com/tab/from-gh-copilot#tab-improvements)Tab Improvements**

The biggest difference is the way Cursor and GitHub Copilot complete code.

GitHub Copilot can insert text at your cursor position. It cannot edit the code around your cursor or remove text.

Cursor can insert text at your cursor, and much more:

- Multi-character edits

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cpp/multi-edit.png

- Instruction-based edits

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cpp/instruct.png

Further, Cursor has a history of your recent changes in the context window, so it knows what you are trying to do next.

### [**](https://docs.cursor.com/tab/from-gh-copilot#migrate-from-github-copilot)Migrate from GitHub Copilot**

Since Cursor comes by default with GitHub Copilot, you might have GitHub Copilot and Cursor installed at the same time. We recommend turning off GitHub Copilot when you want to use Cursor.

By default, Cursor takes precedence over GitHub Copilot. If you want to use GitHub Copilot, you can [**disable Cursor**](https://docs.cursor.com/tab/overview#copilot-settings) in the settings.

## **Advanced Features**

### [**](https://docs.cursor.com/tab/advanced-features#tab-in-peek)Tab in Peek**

You can also use Cursor Tab in the “Go to Definition” or “Go to Type Definition” peek views. This is useful, for example, when adding a new argument to a function call.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cpp/cpp-in-peek.png

We especially enjoy using this in vim in conjunction with **`gd`** to, for example, modify a function definition, then fix all of its usages in one go.

### [**](https://docs.cursor.com/tab/advanced-features#cursor-prediction)Cursor Prediction**

Cursor can also predict where you will go to after an accepted edit. If available, you will be able to press tab to go to the next location, allowing you to tab-tab-tab through edits.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cpp/cp.png

Cursor predicted the next location, and suggested an edit there.

### [**](https://docs.cursor.com/tab/advanced-features#partial-accepts)Partial Accepts**

You can accept the next word of a suggestion by pressing **`Ctrl/⌘`** and the right arrow (or by setting **`editor.action.inlineSuggest.acceptNextWord`** to your preferred keybinding).

To enable partial accepts, navigate to **`Cursor Settings`** > **`Features`** > **`Cursor Tab`**.

# **Chat**

## **Overview**

Cursor Chat lets you ask questions or solve problems in your codebase with the most capable language models, all in your editor.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/chat.png

For language models to give good answers, they need to know specific things that are relevant to your codebase — context.

Cursor has several built in features to provide context in chat, such as automatically including context across your entire codebase, searching the web, indexing documentation, and user-specified references to code blocks. They are built to eliminate the tedious copy-pasting otherwise necessary for working with language models on code.

By default, Cursor Chat is in the AI pane, which is on the opposite side of your primary sidebar. You can toggle the AI pane by pressing **`Ctrl/⌘ + L`**, which focuses onto the chat when opened. To submit your query, press **`Enter`**.

### [**](https://docs.cursor.com/chat/overview#user-and-ai-messages)User and AI Messages**

User messages contain the text you type, along with the context you’ve referenced. You can go back to any previous user messages to edit and rerun your queries. This will overwrite any messages after that and regenerate new ones.

AI messages are the responses generated from the AI model you’ve picked. They are paired with the user message before them. AI messages may contain parsed code blocks which can be added to your codebase with [**instant apply**](https://docs.cursor.com/chat/apply).

All user/AI messages together in the same thread are called a chat thread, and each chat thread is saved in your chat history.

### [**](https://docs.cursor.com/chat/overview#chat-history)Chat History**

By pressing on the “Previous Chats” button on the top right of the AI pane, or by pressing **`Ctrl/⌘ + Alt/Option + L`**, you can see the chat history. You can click on any chat thread to go back and see the messages that make up that thread, and you can also modify the title of the thread by clicking the pen icon, or delete the thread by clicking the garbage can icon upon hovering over the thread in the history.

The title of a Cursor thread is just the first few words of the first user message.

### [**](https://docs.cursor.com/chat/overview#default-context)Default Context**

By default, Cursor Chat includes the current file as context. You can submit a query without including any context by pressing **`Alt/Option Enter`** on submit, or turn on **`Default to no context`** under **`Cursor Settings`** > **`Features`** > **`Chat`**. Chats that begin with a no-context request will not add context for any messages.

As you type, you can see what will be included in context in the pills below the input box.

### [**](https://docs.cursor.com/chat/overview#adding-context)Adding Context**

By default, user messages will contain the text you type, along with the context you’ve referenced. You can add more custom context to each bubble with @ symbols, and by default, the current viewing file will be used as context as well in the user message.

See the [**@ symbols**](https://docs.cursor.com/context/@-symbols/@-files) pages for more information.

### [**](https://docs.cursor.com/chat/overview#ai-fix-in-chat)AI Fix in Chat**

A convenient feature to fix linter errors in your codebase is to use the AI fix in chat. To do this, hover over the error in the editor, and click the blue AI fix button that shows up.

The keyboard shortcut for this would be to do **`Ctrl/⌘ + Shift + E`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/ai-fix.png

### [**](https://docs.cursor.com/chat/overview#long-context-chat-beta)Long Context Chat (Beta)**

You can enable long context chat by going to **`Cursor Settings`** > **`Beta`** > **`Long Context Chat`**. With this enabled, you can toggle different chat modes through **`Ctrl/⌘ .`**.

Long context chat allows you to include entire folders as context, since the supported models have a larger context window. Check out more about the long context only models [**here**](https://docs.cursor.com/advanced/models#long-context-only-models).

## **Customize**

### [**](https://docs.cursor.com/chat/customize#choose-an-ai-model)Choose an AI Model**

Pick your preferred AI model through the [**model toggle**](https://docs.cursor.com/advanced/models#model-dropdown), and Cursor Chat will use that model to generate responses. You can toggle between models by pressing **`Ctrl/⌘ /`**.

By default, Cursor Chat uses OpenAI’s **`GPT-4`** for its AI model (specifically, the **`gpt-4`** label points to our instance of GPT4-Turbo).

The AI model you choose for Chat will be saved for future sessions, so you don’t have to change it every time you open Cursor Chat.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/model-toggle.png

### [**](https://docs.cursor.com/chat/customize#in-editor)In-Editor**

Cursor Chat can also be used as an editor tab by clicking on the horizontal “More” button, and then clicking on the “Open Chat in Editor” button. Cursor Chat will then behave as a regular editor tab. Pressing **`Ctrl/⌘ + L`** will bring up the chat tab and focus onto it.

### [**](https://docs.cursor.com/chat/customize#settings)Settings**

You can customize the Cursor Chat under **`Cursor Settings`** > **`Features`** > **`Chat`**.

These settings include:

- Always search the web for answers.
    - This will make the AI model browse the web each query for the most up-to-date information.
- Add chat fading animation.
    - This adds a smooth animation to the AI messages as they are generated.
- Default to no context.
    - This will make the AI model only use the user message as context, and no additional context such as current file will be included.
- Auto scroll chat.
    - This will automatically scroll the chat as the AI generates text when at the bottom of the thread.
- Narrow scrollbar in the chat pane.
- Show chat history when starting a new chat.

## **With Codebase**

### [**](https://docs.cursor.com/chat/codebase#default-codebase-chat)Default Codebase Chat**

If a codebase isn’t [**indexed**](https://docs.cursor.com/context/codebase-indexing), Cursor Chat will first attempt to compute a few search queries to be used to search across your codebase. For better accuracy, it’s recommended to use [**embeddings search**](https://docs.cursor.com/chat/codebase#embeddings-search).

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/no-embeddings.png

### [**](https://docs.cursor.com/chat/codebase#embeddings-search)Embeddings Search**

With [**codebase indexing**](https://docs.cursor.com/context/codebase-indexing), Cursor Chat can accurately generate responses based on your codebase.

By pressing **`Ctrl/⌘ + Enter`** after typing a message, Cursor Chat scans through your indexed codebase to find pieces of relevant code. This is generally good for quickly including code snippets to be taken into the context of the conversation. For more control over the codebase search and better accuracy, you can use **`@codebase`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/embeddings.png

### [**](https://docs.cursor.com/chat/codebase#advanced-codebase-search)Advanced Codebase Search**

Cursor codebase chat goes through a more detailed search when **`@Codebase`** is used.

See more about **`@Codebase`** [**here**](https://docs.cursor.com/context/@-symbols/@-codebase).

## **Apply**

Cursor’s **`Apply`** allows you to quickly integrate a codeblock suggestion from the chat into your code.

### [**](https://docs.cursor.com/chat/apply#apply-code-blocks)Apply Code Blocks**

To apply a code block suggestion, you can press on the play button in the top right corner of each chat code block.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/apply.png

This will edit your file to incorporate the code produced by Chat. Since you can add the most context and have the most back-and-forth with the model in Chat, we recommend Chat + Apply for more complex AI-driven code changes.

### [**](https://docs.cursor.com/chat/apply#accept-or-reject)Accept or Reject**

Once you have applied a code block, you can go through the diffs and accept or reject the changes. You can also click on the “Accept” or “Reject” buttons in the top right corner of the chat code block.

**`Ctrl/⌘ Enter`** to accept, **`Ctrl/⌘ Backspace`** to reject.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/accept-apply.png

# Cmd K

## **Overview**

Cmd K, also known or “Ctrl K” on Windows/Linux, allows you to generate new code or edit existing code in the editor window.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cmdk/regular.png

### [**](https://docs.cursor.com/cmdk/overview#prompt-bars)Prompt Bars**

In Cursor, we call the bar that appears when you press **`Ctrl/Cmd K`** the “Prompt Bar”. It works similarly to the AI input box for chat, in which you can type normally, or use [**@ symbols**](https://docs.cursor.com/cmdk/context/@-symbols) to reference other context.

### [**](https://docs.cursor.com/cmdk/overview#inline-generation)Inline Generation**

If no code is selected when you press **`Ctrl/Cmd K`**, Cursor will generate new code based on the prompt you type in the prompt bar.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cmdk/generate.png

### [**](https://docs.cursor.com/cmdk/overview#inline-edits)Inline Edits**

For in-place edits, you can simply select the code you want to edit and type into the prompt bar.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cmdk/edit.png

### [**](https://docs.cursor.com/cmdk/overview#follow-up-instructions)Follow-up Instructions**

After each generation, you can further refine the prompt by adding more instructions to the prompt bar, and pressing **`Enter`** so the AI regenerates based on your follow-up instructions.

### [**](https://docs.cursor.com/cmdk/overview#default-context)Default Context**

By default, Cursor will try to find different kinds of useful information to improve code generation, in addition to the manual [**@ symbols**](https://docs.cursor.com/context/@-symbols/@-files) you include.

Additional context may include related files, recently viewed files, and more. After gathering, Cursor ranks the context items by relevance to your edit/generation and keeps the top items in context for the large language model.

### [**](https://docs.cursor.com/cmdk/overview#quick-question)Quick Question**

If you press **`Option/Alt Enter`** while in the prompt bar, Cursor will respond to any questions you have about the selection, and the context you have attached.

The contents of this conversation could be further used in follow-up generations, so you could simply type “do it” after Cursor comes up with a response to generate the code after a quick question.

## **Terminal Cmd K**

In the built-in Cursor terminal, you can press **`Ctrl/⌘ K`** to open a prompt bar on the bottom of the terminal. This prompt bar allows you to describe your desired action in the terminal, and terminal Cmd K will generate a command. You can accept the command by hitting **`esc`** or run the command immediately with **`Ctrl/⌘ + Enter`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/cmdk/terminal-cmdk.png

By default, Terminal Cmd K sees your recent terminal history, your instructions, and anything else you put in the prompt bar as context.

# **Context**

## **Codebase Indexing**

### [**](https://docs.cursor.com/context/codebase-indexing#index-your-codebase)Index your Codebase**

For better and more accurate codebase answers using **`@codebase`** or **`Ctrl/⌘ Enter`**, you can index your codebase. Behind the scenes, Cursor computes embeddings for each file in your codebase, and will use these to improve the accuracy of your codebase answers.

Your codebase index will automatically synchronize with your latest codebase changes.

The status of your codebase indexing is under **`Cursor Settings`** > **`Features`** > **`Codebase Indexing`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/codebase-indexing.png

### [**](https://docs.cursor.com/context/codebase-indexing#advanced-settings)Advanced Settings**

By default, Cursor will index all files in your codebase.

You can also expand the **`Show Settings`** section to access more advanced options. Here, you can decide whether you want to enable automatic indexing for new repositories and configure the files that Cursor will ignore during repository indexing, in addition to your .gitignore settings.

If you have any large content files in your project that the AI definitely doesn’t need to read, [**ignoring those files**](https://docs.cursor.com/context/ignore-files) could improve the accuracy of the answers.

## **Rules for AI**

You can add custom instructions to Cursor by modifying the **`Rules for AI`** section under **`Cursor Settings`** > **`General`** > **`Rules for AI`**.

This custom instruction will be included for features such as Cursor Chat and Ctrl/⌘ K.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/rules-for-ai.png

### [**](https://docs.cursor.com/context/rules-for-ai#cursorrules)`.cursorrules`**

For project-specific instructions, you can include the instructions in a **`.cursorrules`** file in the root of your project.

As the same as the “Rules for AI” section, the instructions in the **`.cursorrules`** file will be included for features such as Cursor Chat and Ctrl/⌘ K.

### **Basic Usage**

In Cursor’s AI input boxes, such as in Cmd K, Chat, or Terminal Cmd K, you can use @ symbols by typing **`@`**. A popup menu will appear with a list of suggestions, and it will automatically filter to only show the most relevant suggestions based on your input.

### [**](https://docs.cursor.com/context/@-symbols/basic#keyboard-shortcuts)Keyboard Shortcuts**

You can navigate through the list of suggestions using the up/down arrow keys. You can hit **`Enter`** to select a suggestion. If the suggestion is a category, such as **`Files`**, the suggestions will be filtered to only show the most relevant items within that category.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@-symbols-basics.png

### [**](https://docs.cursor.com/context/@-symbols/basic#cmd-k-keyboard-shortcut)Cmd K Keyboard Shortcut**

You can use the up/down arrow key to navigate through the list of selected Cmd K @ symbols, **`Enter`** to expand/collapse the selected context item. For file references, you can use **`Ctrl/⌘ M`** to toggle the file reading strategies. Read more about file reading strategies [**here**](https://docs.cursor.com/context/@-symbols/@-files#cmd-k-chunking-strategy).

## @ Symbols

### **@Files**

### [**](https://docs.cursor.com/context/@-symbols/@-files#files)`@Files`**

In AI input boxes such as in Cursor Chat and Cmd K, you can reference entire files by using **`@Files`**. Also, if you continue to type after **`@`**, you will see your file search results after the [**`@Code`**](https://docs.cursor.com/context/@-symbols/@-code) strategy.

In order to make sure the file you’re referencing is the correct file, Cursor will show a preview of the file’s path. This is especially useful when you have multiple files with the same name in different folders.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@file.png

### [**](https://docs.cursor.com/context/@-symbols/@-files#chat-long-file-references)Chat Long File References**

In Cursor’s Chat, if the contents of a file is too long, Cursor will chunk the file into smaller chunks and rerank them based on relevance to the query.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@file-long-file.png

### [**](https://docs.cursor.com/context/@-symbols/@-files#cmd-k-chunking-strategy)Cmd K Chunking Strategy**

For Cmd K, Cursor uses the file references differently based on the content length as well.

- auto
    - Automatically pick one of the three reading strategies based on the file size
- full file
    - The entire file is used as context.
- outline
    - Cursor parses the outline of the file and uses the information as context.
- chunks
    - Cursor chunks the file into smaller chunks and picks the most relevant one.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@file-cmdk.png

### [**](https://docs.cursor.com/context/@-symbols/@-files#drag-and-drop)Drag and Drop**

You can drag and drop files from the primary sidebar into Chat or Cmd K to add them as context as well.

### **@Folders**

Currently, **`@Folders`** is only supported in the Cursor Chat.

### [**](https://docs.cursor.com/context/@-symbols/@-folders#folders)`@Folders`**

You can also reference entire folders in Cursor as context. **`@Folders`** is especially useful for [**long context chat**](https://docs.cursor.com/chat/overview#long-context-chat) where you want to provide a lot of context to the AI.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@folder.png

### **@Code**

### [**](https://docs.cursor.com/context/@-symbols/@-code#code)`@Code`**

To reference specific sections of code, you can use the **`@Code`** symbol.

### [**](https://docs.cursor.com/context/@-symbols/@-code#code-preview)Code Preview**

Similar to the [**`@Files`**](https://docs.cursor.com/context/@-symbols/@-files) symbol, Cursor will show a preview of the code’s content so you can verify that the code you’re referencing is the correct one.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@code.png

### [**](https://docs.cursor.com/context/@-symbols/@-code#from-the-editor)From the Editor**

Another way to add code snippets as context is to select the code you want to reference, and click on either “Add to Chat” (**`Ctrl/⌘ Shift L`**) or “Add to Edit” (**`Ctrl/⌘ Shift K`**).

These will add the selected code snippet to either the Chat input box or the currently active Cmd K prompt bar.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@code-select.png

To add a selected code to a new chat, you can press **`Ctrl/⌘ L`**.

### **@Docs**

### [**](https://docs.cursor.com/context/@-symbols/@-docs#docs)`@Docs`**

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@docs.png

Cursor comes with a set of third party docs crawled, indexed, and ready to be used as context. You can access them by using the **`@Docs`** symbol.

### [**](https://docs.cursor.com/context/@-symbols/@-docs#add-custom-docs)Add Custom Docs**

If you want to crawl and index custom docs that are not already provided, you can do so by **`@Docs`** > **`Add new doc`**. The following modal will appear after you’ve pasted in the URL of your desired doc:

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@docs-add.png

Cursor will then index and learn the doc, and you will be able to use it as context like any other doc.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@docs-learning.png

### [**](https://docs.cursor.com/context/@-symbols/@-docs#manage-custom-docs)Manage Custom Docs**

Under **`Cursor Settings`** > **`Features`** > **`Docs`**, you will see the docs you have added. You can edit, delete, or add new docs here.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@docs-manage.png

### **@Git**

Currently, **`@Git`** is only supported in the Cursor Chat.

### [**](https://docs.cursor.com/context/@-symbols/@-git#git)`@Git`**

In Cursor’s Chat, you can use **`@Git`** to add git commits, diffs, or pull requests to your prompt.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@git.png

### [**](https://docs.cursor.com/context/@-symbols/@-git#common-use-cases)Common Use Cases**

One common use case for **`@Git`** is to allow Cursor’s AI to scan the diff and look for bugs or issues that could be caused by the diff.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@git-usecase1.png

You could also use **`@Diff of Working State`** to generate a commit message from your current diffs.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@git-commit-message.png

### **@Codebase**

### [**](https://docs.cursor.com/context/@-symbols/@-codebase#codebase)`@Codebase`**

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/@codebase.png

Through **`@Codebase`**, Cursor Chat goes through these steps until it finds the most important pieces of code to use.

- Gathering: scanning through your codebase for important files / code chunks
- Reranking: reordering the context items based on relevancy to the query
- Reasoning: thinking through a plan of using the context
- Generating: coming up with a response

Another way of submitting an advanced codebase query is to click on the dropdown next to the **`Ctrl/⌘ + Enter`** button and select **`reranker`** for the search behavior. This is only available when **`@Codebase`** isn’t used, otherwise **`@Codebase`** takes precedence.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/chat/codebase-dropdown.png

### **@Web**

### [**](https://docs.cursor.com/context/@-symbols/@-web#web)`@Web`**

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@web.png

With **`@Web`**, Cursor constructs a search query based on the query and the context you’ve provided, and searches the web to find relevant information as additional context. This is particulary useful for finding the most up-to-date information.

### [**](https://docs.cursor.com/context/@-symbols/@-web#always-on)Always On**

You can make Cursor search the web for chat on every query by turning on “Always search the web” under **`Cursor settings`** > **`Features`** > **`Chat`**. This is equivalent to using **`@web`** on every query.

### **@Chat**

This feature is currently only for Cmd K.

### [**](https://docs.cursor.com/context/@-symbols/@-chat#chat)`@Chat`**

You can add your current chat messages as context by using **`@Chat`** inside Cmd K. This is useful for when you have a conversation with the AI that you’d like to be applied to edit or generate code.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@chat.png

### **@Definitions**

This feature is currently only for Cmd K.

### [**](https://docs.cursor.com/context/@-symbols/@-definitions#definitions)`@Definitions`**

The **`@Definitions`** symbol adds all nearby definitions to Cmd K as context.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@definitions.png

### **Paste Links**

### [**](https://docs.cursor.com/context/@-symbols/@-link#https-your-link-com)`@https://your-link.com`**

In order for Cursor to visit a link before responding, type **`@`** and then paste in the link.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@link.png

### [**](https://docs.cursor.com/context/@-symbols/@-link#remove-links)Remove Links**

By default, we automatically parse links and turn them into **`@Links`** in Cursor Chat. If you prefer to have the link as plain text, click on the link and then click **`Unlink`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/context/@link-unlink.png

### **Ignore Files**

To ignore files to be included in Cursor features such as [**codebase indexing**](https://docs.cursor.com/context/codebase-indexing), you can use a **`.cursorignore`** file in the root of your project. It works the same way as **`.gitignore`** works for git.

**`.cursorignore`** respects **`.gitignore`**. If you already have **`.gitignore`**, the files will be ignored by default. If you want to ignore additional files, you can add them to the **`.cursorignore`** file.

### [**](https://docs.cursor.com/context/ignore-files#example-cursorignore-files)Example `.cursorignore` files**

### [**](https://docs.cursor.com/context/ignore-files#ignore-specific-files)Ignore specific files**

`# Ignore all files in the `dist` directory
dist/

# Ignore all `.log` files
*.log

# Ignore specific file `config.json`
config.json`

### [**](https://docs.cursor.com/context/ignore-files#only-include-specific-files)Only include specific files**

Include only **`*.py`** files in the **`app`** directory. Note that this is the same syntax as **`.gitignore`**.

`# ignore everything
*
# do not ignore app
!app/
# do not ignore directories inside app
!app/*/
!app/**/*/
# don't ignore python files
!*.py`

### [**](https://docs.cursor.com/context/ignore-files#troubleshooting)Troubleshooting**

The ignore file syntax is sometimes a bit confusing. The **`.cursorignore`** file follows the exact same syntax as **`.gitignore`**, so if you are trying an ignore file and it doesn’t work the way you expect it to, we recommend a Google search for the issue, replacing **`cursorignore`** in your search query with **`gitignore`**. Probably someone will have had the same issue and StackOverflow will have a good answer.

One common example: [**here is how you ignore all files except those with a `.php` extension**](https://stackoverflow.com/a/50606028) (just adding **`*`** followed by **`!*.php`** does not work because the gitignore file discoverer will not descend into and discover any **`.php`** files in subdirectories).

# **Advanced**

## **Models**

With Cursor Chat, Ctrl/⌘ K, and Terminal Ctrl/⌘ K, you can easily switch between different models of your choice.

### [**](https://docs.cursor.com/advanced/models#model-dropdown)Model Dropdown**

Underneath the AI input box, you will see a dropdown that allows you to select the model you want to use. By default, Cursor has these models ready to use:

- [**`GPT-4o`**](https://openai.com/index/hello-gpt-4o/)
- [**`GPT-4`**](https://openai.com/index/gpt-4/)
- [**`Claude 3.5 Sonnet`**](https://www.anthropic.com/news/claude-3-5-sonnet)
- **`cursor-small`**
    - **`cursor-small`** is Cursor’s custom model that isn’t as smart as **`GPT-4`**, but is faster and users have unlimited access to it.

You can add additional models under **`Cursor Settings`** > **`Models`** > **`Model Names`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/advanced/model-toggle.png

### [**](https://docs.cursor.com/advanced/models#long-context-only-models)Long Context Only Models**

In long context chat, the model selection is limited to the models that support long context:

- [**`gpt-4o-128k`**](https://platform.openai.com/docs/models)
- [**`gemini-1.5-flash-500k`**](https://deepmind.google/technologies/gemini/flash/)
- [**`claude-3-haiku-200k`**](https://www.anthropic.com/news/claude-3-family)
- [**`claude-3-sonnet-200k`**](https://www.anthropic.com/news/claude-3-family)
- [**`claude-3-5-sonnet-200k`**](https://www.anthropic.com/news/claude-3-5-sonnet)

### [**](https://docs.cursor.com/advanced/models#what-context-window-is-used-for-model-x)What context window is used for model X?**

In chat, we limit to around 20,000 tokens at the moment (or less if the model does not support that much context). For cmd-K, we limit to around 10,000 tokens, to balance TTFT and quality. Long-context chat uses the model’s maximum context window.

## **Custom API Keys**

### [**](https://docs.cursor.com/advanced/api-keys#openai-api-keys)OpenAI API Keys**

Cursor lets you input your own OpenAI API key to send as many AI messages as you want at your own cost.

You can get your own API key from [**here**](https://platform.openai.com/account/api-keys). To use your own API key, go to **`Cursor Settings`** > **`Models`** > **`OpenAI API Key`** and enter your API key. Then, click on the “Verify” button. Once your key is validated, your OpenAI API key will be enabled.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/misc/openai-api.png

### [**](https://docs.cursor.com/advanced/api-keys#anthropic-api-keys)Anthropic API Keys**

Similar to OpenAI, you can also set your own Anthropic API key so that you will be using claude-based models at your own cost.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/misc/anthropic-api.png

### [**](https://docs.cursor.com/advanced/api-keys#google-api-keys)Google API Keys**

For Google API keys, you can set your own API key so that you will be using Google models such as **`gemini-1.5-flash-500k`** at your own cost.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/misc/google-api.png

### [**](https://docs.cursor.com/advanced/api-keys#azure-integration)Azure Integration**

Finally, you can also set your own Azure API key so that you will be using Azure OpenAI models at your own cost.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/misc/azure-api.png

### [**](https://docs.cursor.com/advanced/api-keys#will-my-api-key-be-stored-or-leave-my-device)Will my API key be stored or leave my device?**

Your API key will not be stored, but it will be sent up to our server with every request. All requests are routed through our backend, because that’s where we do the final prompt building.

## **AI Review (Beta)**

AI Review is a feature that allows you to review your recent changes in your codebase to catch any potential bugs.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/advanced/review.png

You can click into individual review items to see the full context in the editor, and chat with the AI to get more information.

### [**](https://docs.cursor.com/advanced/ai-review#custom-review-instructions)Custom Review Instructions**

In order for AI Review to work in your favor, you can provide custom instructions for the AI to focus on. For example, if you want the AI to focus on performance-related issues, you could put:

`focus on the performance of my code`

This way, AI Review will focus on the performance of your code when scanning through your changes.

### [**](https://docs.cursor.com/advanced/ai-review#review-options)Review Options**

Currently, you have a several options to choose from to review:

- **`Review Working State`**
    - This will review your uncommitted changes.
- **`Review Diff with Main Branch`**
    - This will review the diff between your current working state and the main branch.
- **`Review Last Commit`**
    - This will review the last commit you made.

## **Shadow Workspace**

The shadow workspace is an opt-in setting you can configure to improve the quality of AI-generated code. Only some features use it.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/advanced/shadow-workspace.png

If you have the shadow workspace enabled, background AIs can ask for lints for the code they write. This spawns a hidden window locally on your computer, to ensure that your coding experience is unaffected.

The shadow workspace will increase the memory usage from Cursor, so we recommend only enabling this feature if you have plenty of RAM.

You can read more about the shadow workspace in [**our blog post on it**](https://cursor.com/blog/shadow-workspace).

# **Privacy**

## **Privacy FAQ**

### [**](https://docs.cursor.com/privacy/privacy#what-is-privacy-mode)What is Privacy Mode?**

With **`Privacy Mode`** enabled, none of your code will ever be stored by us or any third-party. Otherwise, we may collect prompts, code snippets and telemetry data to improve Cursor. You can [**read more about Privacy Mode here**](https://cursor.com/privacy).

You can enable **`Privacy Mode`** at onboarding or under **`Cursor Settings`** > **`General`** > **`Privacy Mode`**.

!https://mintlify.s3-us-west-1.amazonaws.com/cursor/images/get-started/privacy-mode.png

### [**](https://docs.cursor.com/privacy/privacy#are-requests-always-routed-through-the-cursor-backend)Are requests always routed through the Cursor backend?**

Yes! Even if you use your API key, your requests will still go through our backend! That’s where we do our final prompt building.

### [**](https://docs.cursor.com/privacy/privacy#does-indexing-the-codebase-require-storing-code)Does indexing the codebase require storing code?**

It does not! If you choose to index your codebase, Cursor will upload your codebase in small chunks to our server to compute embeddings, but all plaintext code ceases to exist after the life of the request.

The embeddings and metadata about your codebase (hashes, obfuscated file names) are stored in our database, but none of your code is.

You can read more about this on our [**security page**](https://cursor.com/security).

# **Troubleshooting**

## **Common Issues**

### [**](https://docs.cursor.com/troubleshooting/common-issues#i-see-an-update-on-the-changelog-but-cursor-wont-update)I see an update on the changelog but Cursor won’t update.**

If the update is very new, it might not have rolled out to you yet. We do staged rollouts, which means we release new updates to a few randomly selected users first before releasing them to everyone. Typically, reaching all users takes around 5 hours from the first user. For larger updates, it can take longer.

### [**](https://docs.cursor.com/troubleshooting/common-issues#i-have-issues-with-my-github-login-in-cursor-how-do-i-log-out-of-github-in-cursor)I have issues with my GitHub login in Cursor / How do I log out of GitHub in Cursor?**

You can try using the **`Sign Out of GitHub`** command from the command palette **`Ctrl/⌘ + Shift + P`**.

### [**](https://docs.cursor.com/troubleshooting/common-issues#i-cant-use-github-codespaces)I can’t use GitHub Codespaces.**

Unfortunately, we don’t support GitHub Codespaces yet.

### [**](https://docs.cursor.com/troubleshooting/common-issues#i-have-errors-connecting-to-remote-ssh)I have errors connecting to Remote SSH.**

Currently, we don’t support SSHing into Mac or Windows machines. If you’re not using a Mac or Windows machine, please report your issue to us in the [**forum**](https://forum.cursor.com/). It would be helpful to include some logs for better assistance.

### [**](https://docs.cursor.com/troubleshooting/common-issues#cursor-tab-and-cmd-k-do-not-work-behind-my-corporate-proxy)Cursor Tab and Cmd K do not work behind my corporate proxy.**

Cursor Tab and Cmd K use HTTP/2 by default, which allows us to use less resources with lower latency. Some corporate proxies (e.g. Zscaler in certain configurations) block HTTP/2. To fix this, you can set **`"cursor.general.disableHttp2": true`** in the settings (**`Cmd/Ctrl + ,`** and then search for **`http2`**).

### [**](https://docs.cursor.com/troubleshooting/common-issues#i-just-subscribed-to-pro-but-i-m-still-on-the-free-plan-in-the-app)I just subscribed to Pro but I’m still on the free plan in the app.**

Try logging out and logging back in from the [**Cursor Settings Popup**](https://docs.cursor.com/get-started/glossary#cursor-settings-popup).

### [**](https://docs.cursor.com/troubleshooting/common-issues#when-will-my-usage-reset-again)When will my usage reset again?**

If you’re subscribed to Pro you can click on **`Manage Subscription`** from the [**Dashboard**](https://cursor.com/settings) and your plan renewal date will be displayed at the top.

If you’re a free user you can check when you got the first email from us in your inbox. Your usage will reset every month from that date.

### [**](https://docs.cursor.com/troubleshooting/common-issues#how-do-i-uninstall-cursor)How do I uninstall Cursor?**

You can follow [**this guide**](https://code.visualstudio.com/docs/setup/uninstall) to uninstall Cursor. Replace every occurrence of “VS Code” or “Code” with “Cursor”, and “.vscode” with “.cursor”.

## **Troubleshooting Guide**

The following is a list of information that is helpful to retrieve for most troubleshooting scenarios within Cursor:

**01)** Screenshot of issue (redact any sensitive information)

**02)** Steps to reproduce

**03)** System Information from:

**`Cursor`** > **`Help`** > **`About`**

**04)** Are you using a VPN or Zscaler?

**05)** Developer tools console errors

Open developer tools via:

**`Cursor`** > **`Help`** > **`Toggle Developer Tools`**

and then click **`Console`** and see if there are any related errors.

**06)** Logs

On Windows, you can find logs here:

`C:\Users\<your-user-name>\AppData\Roaming\Cursor\logs`

This is the parent folder of the folder that is opened when doing:

- **`Ctrl`** + **`Shift`** + **`P`** (to open command palette in Cursor)
- Typing and selecting **`Developer: Open Logs Folder`**

You can also view logs in **`Cursor`** > **`Terminal`** > **`Output`** and then click on the dropdown and select **`Window`** or one of the other Cursor specific options, such as **`Cursor Tab`** or **`Cursor Indexing & Retrieval`**.