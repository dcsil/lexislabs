# Use Cases

## 1. Reading karaoke

### User interaction

The user is shown a button to begin mic input and instructions to read aloud a displayed text in their target learning language (e.g. a short story).
Upon pressing the button and beginning reading, pronunciation feedback for read sentences will be displayed incrementally.
The user can click on feedback items for more detailed or graphical explanations of their errors.

### Technical implementation

The backend app will retrieve a short text in the user's target language either from our Postgres DB or by requesting a generated text from Cohere's Aya LLM, which factors in the user's previous assessments and level of proficiency. The frontend app will inject the text into the appropriate visual element.

Upon beginning mic input, the user's speech is streamed to the backend, which streams it to the Azure Speech AI Pronunciation Assessment API. The reference text is also sent to Azure. As feedback is returned from Azure, the backend will forward the updated scores and incremental feedback for the frontend to display.

When the user closes the app or exits the assessment, the frontend notifies the backend to persist parts of the assessment (e.g. fluency score, incorrectly pronounced words) to the user's profile in the DB.

### UI sketch

<p align="center">
  <img src="./assets/Reading_karaoke.png" />
  <br>
  <em>Figure 1: Reading karaoke UI sketch</em>
</p>

## 2. Long reading

### User interaction

The user is shown a button to begin mic input and instructions to read aloud a displayed long text in their target learning language _without interruption_.
Upon pressing the button and beginning reading, the text will autoscroll to keep the text on-screen.

Once the user finishes reading the text, feedback will be displayed about pronunciation of the entire text. The user can click on a highlighted overlay of the read text for more detailed or graphical explanations of specific errors.

### Technical implementation

The backend app will retrieve a long text in the user's target language either from our Postgres DB or by requesting a generated text from Cohere's Aya LLM, which factors in the user's previous assessments and level of proficiency. The frontend app will inject the text into the appropriate visual element.

Upon beginning mic input, the user's speech is streamed to the backend, which streams it to the Azure's pronunciation assessment API. The reference text is also sent to Azure. When the user finishes reading, the backend requests a pronunciation assessment report from Azure, and parses it in preparation for the frontend to display feedback to the user. The report and its associated metrics are also saved to the user's profile in our DB.

### UI sketch

<p align="center">
  <img src="./assets/Long_reading.png" />
  <br>
  <em>Figure 2: Long reading UI sketch</em>
</p>

## 3. Convobot

### User interaction

Within a conversational interface, the user is presented with a button to begin mic input and start a conversation with an automated agent. After pressing the button, the user can start talking about a topic of their choice. After pausing a significant duration or by manually pressing the mic button again, the user's speech is transcribed to text that is displayed as a chat bubble on the screen. After a short time, the agent responds to the user's utterance in the form of a new chat bubble.

The user can then press the mic button again to say something, and continue this conversation indefinitely.

The user can access a side panel that displays their pronunciation performance during the active conversation. The panel can be opened at any point during the conversation and doesn't interrupt the conversation.

### Technical implementation

After receiving the user's initial speech input, a recording of their speech is saved to our Postgres DB. Meanwhile, the recording is also sent to Azure's fast transcription API, and the resulting transcription is displayed to the user. The transcription is also sent to Cohere's Aya LLM to generate a conversational response, which is displayed to the user as the agent's response. This process repeats every time the user provides speech input.

At regular intervals in the background, recordings of the user's input are sent in batches to Azure's pronunciation assessment API, and subsequently deleted from our DB. The assessment results, alongside the transcriptions of user's input and the agent's responses, are saved in our DB as a historical record of the conversation.

Upon opening the side panel, the user's pronunciation performance is retrieved from our DB and displayed by the frontend. If there are outstanding recordings which haven't been sent for assessment yet, the user is offered to force a manual update of their performance report.

### UI sketch

<p align="center">
  <img src="./assets/Convobot.png" />
  <br>
  <em>Figure 3: Convobot UI sketch</em>
</p>

## 4. Progress dashboard

### User interaction

A visually appealing dashboard presents statistics about the user's current pronunciation proficiency and their usage of the app. This can include graphs showing historical assessment scores, comparisons to standardized language learning guidelines, and summaries about areas in need of improvement.

### Technical implementation

The backend requests the necessary user data from the DB, and generates a data structure that contains all the statistics to be displayed. The frontend parses the data structure to populate graphical elements. The frontend should cache the report to reduce demand on BE resources if the user frequently opens the dashboard page.

### UI sketch

<p align="center">
  <img src="./assets/Progress_dashboard.png" />
  <br>
  <em>Figure 4: Progress dashboard UI sketch</em>
</p>
