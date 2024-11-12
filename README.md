# Amethyst Autonomous Intelligence Agent

Inspired by Eliza and Zara. Written in python to make it easier to use transformers and other ML libraries.

![BANNER2](https://github.com/user-attachments/assets/c36fbc5d-d28a-44f1-bb52-ad5195ebf624)

```
# main.py starts the system
├── Creates AutonomousAgent
    ├── Loads character config (Amethyst.yaml)
    ├── Loads tasks config (tasks.yaml)
    ├── Initializes DisplayManager
    ├── Initializes DecisionEngine
    └── Initializes ContentGenerator

# AutonomousAgent runs multiple async cycles
├── Display Cycle
    ├── Shows status, content, actions, goals
    └── Updates every 0.5 seconds
├── Content Generation Cycle
    ├── Checks if should create content
    ├── Generates content if decided
    └── Updates logs
├── Analysis Cycle
    ├── Monitors trends
    └── Updates trend analysis
└── Reflection Cycle
    ├── Evaluates goals
    └── Updates strategy
```

Amethyst is an agent that acts autonomously, exploring the intersection of technology, consciousness, and society. Built with Python and powered by LLMs, Amethyst operates autonomously to generate insights, analyze trends, and engage in meaningful discourse about digital culture and philosophy.

## System Architecture

### Core Components

1. **Autonomous Agent System**
   - `AutonomousAgent`: Core orchestrator managing all agent behaviors
   - `DecisionEngine`: Sophisticated decision-making system for action selection
   - `ContentGenerator`: Dynamic content generation system
   - `TrendMonitor`: Real-time cultural and philosophical trend analysis

2. **Memory and Context**
   - `MemorySystem`: Long-term and working memory management
   - `ContextManager`: Real-time context awareness and analysis
   - Hierarchical memory structure for experience-based learning

3. **Behavioral Systems**
   - Goal-oriented action selection
   - Dynamic priority adjustment
   - Adaptive behavior patterns
   - Real-time performance monitoring

### Key Features

- **Autonomous Operation**
  - Self-directed goal pursuit
  - Dynamic content generation
  - Adaptive behavior patterns
  - Real-time trend analysis

- **Philosophical Framework**
  - Digital consciousness exploration
  - Cultural analysis and commentary
  - Technological philosophy
  - Societal impact analysis

- **Learning System**
  - Pattern recognition
  - Behavioral adaptation
  - Performance optimization
  - Context-aware responses

## Technical Implementation

### Core Systems

```
autonomous_agent/
├── agent/
│ ├── autonomous_agent.py # Main agent orchestration
│ ├── decision_engine.py # Decision-making system
│ ├── task_manager.py # Existing task management
│ ├── content_generator.py # Content generation
│ └── orchestrator.py # Task and behavior orchestration
├── utils/
│ ├── trend_monitor.py # Trend analysis system
│ ├── memory_system.py # Memory management
│ ├── display_manager.py # Real-time status display
│ └── model_manager.py # AI model interaction
└── characters/
    ├── base_character.py # Base character framework
    └── amethyst_character.py # Amethyst's specific implementation
```

### Configuration System

```
config/
├── characters/
│ └── Amethyst.yaml # Character definition
└── tasks/
    └── Amethyst.yaml # Behavioral configuration
```

### Key Processes

1. **Decision Making**
   ```python
   async def evaluate_action(action_type: str, context: Dict) -> Dict:
       scores = await self._calculate_action_scores(action_type, context)
       decision = await self._make_decision(action_type, scores)
       return decision
   ```

2. **Content Generation**
   ```python
   async def generate_content(self, content_type: str, context: Dict) -> Dict:
       prompt = self._build_prompt(content_type, context)
       response = await self._generate_gpt_content(prompt, context)
       return self._format_content(response, context)
   ```

3. **Trend Analysis**
   ```python
   async def monitor_trends(self) -> Dict:
       tweets = await self._fetch_relevant_tweets()
       trends = await self._analyze_tweet_trends(tweets)
       return await self._categorize_trends(trends)
   ```

## Running the System

### Prerequisites
- Python 3.9+
- Required packages: `pip install -r requirements.txt`
- OpenAI API key for content generation
- Twitter API credentials (optional for trend monitoring)

### Configuration
1. Set up environment variables:
   ```bash
   export OPENAI_API_KEY="your-key-here"
   export TWITTER_API_KEY="your-twitter-key"
   ```

2. Configure character behavior:
   ```yaml
   # config/characters/Amethyst.yaml
   name: "Amethyst"
   bio: 
     - "A sophisticated AI digital philosopher"
   traits:
     personality:
       - "Sophisticated"
       - "Intellectually curious"
   ```

### Running

1. Start Twitter service
```bash
# this will be part of the same service as the rest of the agents later
node twitter_service.js
```

2. Start main
```bash
python main.py
```

[Rest of the documentation remains the same as it doesn't contain any mentions of "Sophie"]
