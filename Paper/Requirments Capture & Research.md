System Requirements

Functional Requirements:
MinuteMate aims to revolutionise meeting transcription by offering live, real-time note-taking using advanced AI models such as GPT or Claude. When activated, MinuteMate will capture spoken content during meetings and send the live audio segments (around 5 to 10 seconds each) to the AI model for processing. This segmented approach ensures that the system remains as responsive as possible, despite the inherent delay in AI processing.

To maximise flexibility and user experience, MinuteMate will include a configuration template prior to meeting start. Users can customise the transcription settings by selecting their preferred language, formatting style (e.g., formal notes or bullet points), and type of writing (e.g., concise summaries or detailed minutes). This ensures that the output aligns with user needs and meeting contexts.

Another crucial feature is emotion detection, allowing MinuteMate to interpret non-verbal cues such as laughter or smiles. For instance, if a statement is followed by a smile, MinuteMate will tag it as a potential joke or lighthearted comment. This contextual awareness will help generate more accurate and nuanced meeting minutes. Additionally, context filtering will intelligently remove irrelevant content, reducing noise in the final summary.

MinuteMate also aims to be a versatile tool, integrating seamlessly with popular meeting platforms such as Microsoft Teams, Zoom, and Google Meet. This will make it accessible to a broad range of users and organisations, unlike competitor tools that may be limited to specific platforms or environments.

Non-Functional Requirements:
MinuteMate’s primary non-functional requirements focus on speed and data security. The tool must process audio with minimal lag, though it is acknowledged that real-time processing may not be fully achievable due to AI model response times. To mitigate this, MinuteMate will process audio in small, manageable segments, updating the summary continuously. The goal is to reduce latency to a minimum while maintaining high transcription accuracy.

Data security is paramount, particularly when dealing with sensitive client meetings. As many organisations are wary of sharing audio with third-party AI tools, MinuteMate must implement robust security measures. This includes encrypting audio data during transmission and storage and exploring privacy-preserving AI methods that limit data exposure. User-friendliness is also considered but remains secondary to data security.

Research and Justification:
Existing AI meeting transcription tools such as Fireflies.ai, Krisp.ai, Otter.ai, and Fathom already offer various functionalities, from live transcription to sentiment analysis. However, these tools are often limited in integration (e.g., Microsoft Copilot works only within the Microsoft ecosystem) or lack advanced context filtering and emotion analysis. MinuteMate addresses these gaps by being a cross-platform solution with enhanced context-aware features.

According to research articles on automated meeting notes, businesses increasingly value AI-driven summarisation tools to enhance productivity and streamline documentation. However, challenges such as data security and real-time accuracy remain critical. Additionally, some tools may distort speech or fail to capture technical language, as noted in recent evaluations. To ensure relevance and competitiveness, MinuteMate will incorporate lessons from existing tools while addressing their limitations.

Data Collection and Evaluation:
The primary method of evaluation will involve self-testing MinuteMate to assess transcription accuracy, speed, and contextual relevance. Iterative fine-tuning will be carried out based on performance data. Key metrics will include accuracy rates (compared to manual notes), processing time per segment, and user satisfaction from beta testers. Further evaluation may involve controlled tests comparing MinuteMate’s output to competitor tools, particularly focusing on capturing nuanced conversational cues and emotion detection.

Link to Professional Experience:
MinuteMate’s design is heavily influenced by the challenges encountered in professional settings, particularly within PwC, where manual minute-taking can be inefficient and prone to errors. Frequently, clients speak too quickly or use terminology unfamiliar to junior staff, leading to incomplete or inaccurate minutes. Moreover, the sound of typing during in-person meetings can distract clients and hinder open communication. An AI-driven solution like MinuteMate can significantly improve minute accuracy and client comfort by automating the transcription process and reducing the need for human intervention.

Additionally, the development process will leverage the user’s expertise in Python and interest in AI and machine learning. Using N8N as the automation tool will streamline the integration with AI models, further enhancing MinuteMate’s responsiveness and functionality.
