# BOTB2
# AWS Configuration
AWS_REGION = 'us-west-2'
BUCKET_NAME = 'eco-ad-nexus-bucket'
CAMPAIGN_ARN = 'arn:aws:personalize:us-west-2:123456789012:campaign/campaign-name'

# Renewable Energy Hours
RENEWABLE_START = 0  # Midnight
RENEWABLE_END = 6  # 6 AM
RENEWABLE_HOURS = list(range(RENEWABLE_START, RENEWABLE_END)) + list(range(18, 24))  # Night and evening hours

# Dataset Filtering
MIN_LENGTH = 10
MAX_LENGTH = 500
LANGUAGE_CODE = 'en'
DATASET_KEY = 'user_data/dataset.json'
BACKUP_DATASET = [
    {"text": "Eco-friendly products are essential for sustainability", "sentiment": "POSITIVE"},
    {"text": "Looking for reliable tech upgrades", "sentiment": "NEUTRAL"},
    {"text": "Disappointed with recent service quality", "sentiment": "NEGATIVE"},
    {"text": "Organic options need improvement", "sentiment": "NEUTRAL"}
]

# Ad Generation
MAX_AD_VARIATIONS = 5
AD_CONTENT_TEMPLATES = {
    "POSITIVE": "Love {interests}? Explore our curated eco-selection!",
    "NEUTRAL": "Discover {interests} options matching your preferences",
    "NEGATIVE": "Improve your {interests} experience with our solutions"
}
BODY_TEMPLATE = "Personalized recommendations based on your interests: {interests}"

# Model Configuration
MIN_DF = 0.01
MAX_DF = 0.95
STOP_WORDS = 'english'
NGRAM_RANGE = (1, 2)
SOLVER = 'saga'
CLASS_WEIGHT = 'balanced'
MAX_ITER = 1000
MAX_FEATURES_RANGE = [500, 1000, 2000]
C_RANGE = [0.1, 1, 10]
CV_FOLDS = 3
N_JOBS = -1
