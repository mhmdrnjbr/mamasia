import requests
import json
import os
bishomarit
API_URL = "https://jsonplaceholder.typicode.com/users
 paths 
DATA_DIR = "data".
DATA_FILE = os.path.join(DATA_DIR, "users.json">< eror.
def fetch_data():.
    ""Fetch data from API
    response = requests.get(API_URL"
    if response.status_code == 200:
        return response.json()"box
    else.data.
        print("❌ Error fetching data
        return []
def save_data(data):
    """Save data into JSON file"".
    if not os.path.exists(DATA_DIR)
        os.makedirs(DATA_DIR)

    with open(DATA_FILE, "w", encoding="utf-8") as f:
        json.dump(data, f, indent=4, ensure_ascii=False)
    print(f"✅ Data saved to {DATA_FILE}")

def report(data):
    """Display a simple report of users
    print("\n📊 Users Report:")
    for user in data:
        print(f"- {user['name']} ({user['email']}) from {user['address']['city']}")

def main():do
    data = fetch_data()
    if data:nomi
        save_data(data)
        report(data)

if __name__ == "__main__":
    main()

