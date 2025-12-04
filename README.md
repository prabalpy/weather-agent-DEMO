# Convlyze AI

An intelligent multilingual audio analysis system that transcribes, validates, and analyzes audio conversations using Google's Gemini AI models. The system provides comprehensive insights including transcript generation, SOP compliance evaluation, sentiment analysis, performance scoring, and automated report generation.

## Performance

- **Average Processing Time**: 30-90 seconds (depending on audio length)
- **Concurrent Analysis**: 7 parallel analysis tasks
- **Retry Logic**: 3 attempts with exponential backoff
- **Rate Limiting**: Built-in API rate limit handling with smart delays

## Language Support

| Language | Code | Language | Code |
|----------|------|----------|------|
| English | en | Japanese | ja |
| Hindi | hi | Korean | ko |
| Spanish | es | Arabic | ar |
| French | fr | Russian | ru |
| German | de | Portuguese | pt |
| Chinese | zh | Italian | it |

## Project Structure

```
convlyze-ai/
├── main.py                 # Main analyzer class and pipeline
├── map.py                  # SOP to Q&A mapping
├── score.py                # SOP scoring logic
├── prompts.py              # AI prompt management
├── pdfgeneration.py        # Report generation
├── requirements.txt        # Python dependencies
├── .env                    # Environment variables
└── README.md              # Documentation
```

## Error Handling

- **Retry Logic**: Automatic retries for 503/429 errors with exponential backoff
- **Safe JSON Parsing**: Handles malformed responses with fallback mechanisms
- **File Cleanup**: Automatic temporary file removal on success/failure
- **Graceful Degradation**: Returns partial results if individual analyses fail
- **Exception Logging**: Comprehensive error tracking for debugging
