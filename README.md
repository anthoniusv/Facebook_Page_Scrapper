## **Facebook Page Scraper**

This project retrieves **Facebook page details** and **Facebook post details** using the **RapidAPI Facebook Pages Scraper**. The data is saved as JSON files, which can later be converted to CSV.

---

### **Prerequisites**
1. Install required libraries using pip:
   ```bash
   pip install requests pandas
   ```
2. A valid **RapidAPI key**:
   - Get the key by subscribing to [RapidAPI](https://rapidapi.com).

---

### **How to Use**

1. **Update the API Key**:
   Replace the placeholder in the script with your **RapidAPI key**.

   ```python
   headers = {
       "x-rapidapi-host": "facebook-pages-scraper2.p.rapidapi.com",
       "x-rapidapi-key": "YOUR_API_KEY_HERE"
   }
   ```

2. **Update the Facebook Page Link**:
   Replace `YourPageName` with the Facebook page you want to scrape.

   ```python
   params = {"link": "https://www.facebook.com/YourPageName"}
   ```

3. **Run the Script**:
   - **Page Details**:
     This script retrieves the Facebook page details:
     - Output: `facebook_page_details.json`

   - **Post Details**:
     This script retrieves the Facebook post details:
     - Output: `facebook_posts.json`

---

### **Columns in the CSV**

#### **Page Details CSV**

| Column Name            | Description                                  |
|-------------------------|----------------------------------------------|
| `about_me_text`        | Page's short "About" description.            |
| `about_me_text_content`| Full "About Me" content.                     |
| `ad_status`            | Indicates if the page is running ads.        |
| `address`              | Physical location or address of the page.    |
| `bio`                  | Additional biography information.            |
| `business_price`       | Price range for business services.           |
| `category`             | Categories assigned to the page (e.g., Petrol Station). |
| `creation_date`        | Date the page was created.                   |
| `description`          | Full page description or bio.                |
| `email`                | Contact email of the page.                   |
| `followers_count`      | Total number of followers.                   |
| `likes_count`          | Total number of page likes.                  |
| `phone`                | Contact phone number.                        |
| `rating`               | User rating (if available).                  |
| `website`              | Link to the page's website.                  |

---

#### **Post Details CSV**

| Column Name          | Description                                  |
|-----------------------|----------------------------------------------|
| `post_id`            | Unique ID of the post.                      |
| `post_link`          | Direct link to the Facebook post.           |
| `text`               | Content of the post.                        |
| `share_count`        | Number of times the post was shared.        |
| `comments_count`     | Number of comments on the post.             |
| `total_reaction_count` | Total reactions (sum of all reactions).   |
| `like_count`         | Number of "Like" reactions.                 |
| `haha_count`         | Number of "Haha" reactions.                 |
| `love_count`         | Number of "Love" reactions.                 |
| `care_count`         | Number of "Care" reactions.                 |
| `publish_time`       | Time the post was published (converted to WIB). |
| `media_type`         | Type of media in the post (e.g., Photo).    |
| `media_url`          | URL of the media (e.g., image link).        |

---

### **Important Notes**
- You **must update** the API key and Facebook page link before running the script.
- Ensure your usage complies with **RapidAPI** and **Facebook policies**.
- The API key must **not** be shared publicly.

---

### **License**
This project is licensed under the MIT License.  
