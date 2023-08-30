```python
# oracle_ai_assistant/tech_stack.py

class TechStack:
    def __init__(self):
        self.programming_languages = ["Python", "JavaScript", "TypeScript"]
        self.frameworks = ["Django", "Flask", "React", "Node.js", "Express.js"]
        self.libraries_and_tools = ["TensorFlow", "PyTorch", "NLTK", "spaCy", "Transformers", "Docker", "Kubernetes"]
        self.databases = ["PostgreSQL", "MongoDB", "Redis"]

    def get_programming_languages(self):
        return self.programming_languages

    def get_frameworks(self):
        return self.frameworks

    def get_libraries_and_tools(self):
        return self.libraries_and_tools

    def get_databases(self):
        return self.databases

tech_stack = TechStack()
```