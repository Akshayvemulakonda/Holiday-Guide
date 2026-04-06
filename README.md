# Holiday-Guide
from recommender import recommend_destination
from utils import display_results

def get_user_preferences():
    print("🌍 Welcome to Holiday Guide\n")

    travel_type = input("Enter preferred destination type (beach/mountain/city/nature): ").lower()
    budget = input("Enter budget (low/medium/high): ").lower()
    activity = input("Enter preferred activity (relaxation/adventure/culture/nightlife/snow): ").lower()

    return {
        "type": travel_type,
        "budget": budget,
        "activity": activity
    }

def main():
    preferences = get_user_preferences()
    results = recommend_destination(preferences)
    display_results(results)

if __name__ == "__main__":
    main()
