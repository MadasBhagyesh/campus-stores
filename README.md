# Campus Stores

Campus Stores is a Product Engineer work sample set at a fictional campus media equipment desk. Work through a club’s screening, from equipment pickup to a partial return and the next morning’s handover. Open **Candidate brief** in the app for the assignment.

## Run the app

Open `index.html` in a modern browser. The app includes its scripts, styles, and icons and can run offline.

To serve it over local HTTP, run this from the repository folder and visit `http://localhost:8000`.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Each browser stores its own sample shift locally when browser storage is available. **Restart sample shift** restores the fictional starting records.

## Work sample

### Product decision: Keep Campus Stores
I would keep Campus Stores.

- **What the product handles well:** At Friday's partial return (7:30 pm), issuing one slip per physical unit lets the clerk close the projector (PR-04) and speaker (SP-02) slips while keeping the adapter (AD-12) outstanding.
- **What needed to change:** During the Saturday morning handover (9:00 am), Leela brings back the adapter. The Desk book note states Leela will return it at 9 a.m., but the Loan register identifies the adapter by its asset tag (AD-12) and original collector (Kabir Sen). Without a direct link, the incoming clerk must manually connect the unstructured note to the register slip to choose the right record to close.
- **The prototype:** Added **Return follow-ups** to the Desk book, linking an outstanding slip directly to the expected returner and time. The morning clerk can verify the asset tag and click **View slip** to immediately jump to and highlight the matching loan slip in the register. Closing the slip automatically resolves the follow-up while preserving the original collector audit trail.

### Try the Film Society shift

1. Click **Restart sample shift**. In **Requests**, open the Film Society form (RQ-214). Check the **Desk book** for Kabir's pickup authorization.
2. In **Loan register**, issue **PR-04**, **SP-02**, and **AD-12** on separate issue slips to **Kabir Sen** for **RQ-214**, each due **Fri 8 pm**.
3. Click **Move to return time**. Record the return of **PR-04** and **SP-02**. In **Desk book**, select **AD-12** under **Return follow-ups**, enter **Leela Das** and **Sat 9 am**, and save.
4. Click **Move to next morning**. In **Desk book**, find the **AD-12** follow-up for Leela Das and click its **View slip** button. Verify the adapter's physical tag against the highlighted row in **Loan register**, then click **Record return** on that row.
5. Return to **Desk book** and confirm the AD-12 follow-up says **Resolved**. The Debate Union microphone should still be outstanding in **Loan register**.

### What I would observe at a real counter

I would watch whether the incoming clerk can use the physical asset tag to identify and close the correct slip on the first attempt without asking the previous shift for help.

## Source

- `index.html` contains the desk layout, candidate brief, and bundled icons.
- `app.js` contains the sample records and interactions.
- `styles.css` defines the desktop and mobile layouts.

Icon license notices are in [third-party/lucide-LICENSE.txt](third-party/lucide-LICENSE.txt).


## Submit your work

1. [Fork Campus Stores](https://github.com/virinchi-healthcare/campus-stores/fork) into your GitHub account. Complete the candidate brief and push your changes to your public fork. In your README, point reviewers to your work and explain the decision you made.
2. In your fork, open **Commits**, select the final commit you want reviewed, and copy the page URL. It should look like `https://github.com/YOUR-USERNAME/campus-stores/commit/COMMIT-SHA`.
3. [Submit your work through the Google Form](https://docs.google.com/forms/d/e/1FAIpQLScvzoh1R4WS-SkiwAVBQbMvniieJYSoOEfLMyVo5CyjOvYUgQ/viewform). Your **roll number**, **email ID**, and **final commit link from your public fork** are required. Enter your roll number and email ID in the form only.
