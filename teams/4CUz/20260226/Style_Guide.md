# **STYLE\_GUIDE.md — Tripable**

Purpose: Define the visual identity for Tripable so every page, screen, and asset feels cohesive with the current website. This guide should help designers, developers, and future contributors keep the product consistent as new features are added.

---

## **1\. Visual Tone**

Overall feel: Warm, social, and organized; a trip-planning space that feels easy to use, friendly to share, and built for groups making decisions together.

“Plan the trip together, without losing the details in the group chat.”

What it is: Friendly, Collaborative, Clean, Travel-inspired, Trustworthy

What it is not: Corporate travel software, Overly formal, Cluttered dashboard, Generic booking site, Heavy productivity tool

---

## **2\. Color Palette**

| Name | Hex | Role |
| ----- | ----- | ----- |
| \[Primary\] | \#1E4840  | Main brand color — navigation, primary buttons, key actions, important headings |
| \[Secondary\] | \#BAF59C  | Supporting brand color — highlights, positive states, selected items, soft emphasis |
| \[Accent\] | \#F4C95D  | Small moments of emphasis — badges, reminders, pending items, and callouts |
| \[Background\] | \#ECF5E9 | Main page background — gives the product a light, calm, travel-friendly feel |
| \[Text\] | \#18332E | Main text and headings — softer than pure black, but still high contrast |
| \[Error\] | \#D9534F | Conflicts, unavailable dates, destructive actions, and form errors |

### **Color Rules**

* Use dark green as the main anchor color. It should make Tripable feel calm, grounded, and trustworthy.  
* Use light green as a friendly highlight, not as the main text color.  
* Keep backgrounds soft and warm instead of stark white whenever possible.  
* Use white cards on the light green background to make important content feel organized.  
* Avoid pure black (\#000000). Use \#18332E for headings and body text.  
* Make sure body text and buttons meet WCAG AA contrast standards.

Use color to signal group interaction:

* Light green → selected, agreed, confirmed, or positive group consensus  
* Yellow → pending decisions, reminders, or items that need attention  
* Red → conflicts, unavailable dates, errors, or destructive actions  
* Muted gray-green → secondary information, inactive states, or helper text

---

## **3\. Typography**

Heading font: Inter or a clean rounded sans-serif

Body font: Inter

### **Type Scale**

| Style | Size | Weight | Usage |
| ----- | ----- | ----- | ----- |
| H1 | 2.25rem | Bold | Hero headline, main page title |
| H2 | 1.75rem | Bold | Section titles and major feature headers |
| H3 | 1.375rem | Semibold | Card titles, dashboard sections, smaller feature headers |
| Body | 1rem | Regular | Paragraphs, descriptions, form copy, general interface text |
| Small | 0.875rem | Regular | Labels, captions, helper text, metadata |
| Button | 0.95rem | Semibold | Primary and secondary actions |

### **Typography Rules**

* Keep headlines short, clear, and benefit-focused.  
* Use natural language instead of startup jargon.  
* Body copy should feel like helpful product guidance, not a marketing essay.  
* Use sentence case for most interface labels.  
* Avoid long blocks of text inside cards; break information into clear actions or short descriptions.

---

## **4\. Component Patterns**

### **Buttons**

| Type | Style | Usage |
| ----- | ----- | ----- |
| Primary CTA | Filled dark green, light text, rounded corners | Create a trip, start planning, save a decision, continue |
| Secondary | White or transparent background, dark green border/text | Invite friends, view details, edit trip info |
| Soft CTA | Light green background, dark green text | Confirm, select, vote, mark available |
| Destructive | Red text or red outline, used sparingly | Delete trip, remove member, clear response |

Button rules:

* Primary buttons should be easy to find but not overly loud.  
* Use rounded corners to match the friendly brand feel.  
* Keep button labels action-oriented: “Create trip,” “Invite friends,” “Add dates,” “Save plan.”  
* Avoid vague labels like “Submit” when a more specific action is possible.

### **Cards**

* Background: white  
* Border radius: 16–20px  
* Border: subtle \#DCE8DE when needed  
* Shadow: soft and minimal  
* Padding: 20–24px

Used for:

* Trip overview  
* Destination cards  
* Availability summaries  
* Itinerary items  
* Expense items  
* Group decisions

Card Rules: 

* Cards should make planning feel organized, not crowded.  
* Each card should have one clear purpose.  
* Use images sparingly and only when they help create a travel feeling.  
* Keep important actions visible without overwhelming the card.

### **Form Inputs**

* Background: white  
* Border radius: 12px  
* Border: \#DCE8DE  
* Focus state: dark green outline or ring  
* Placeholder text: \#8A9A95

Examples:

* Trip name  
* Destination  
* Dates  
* Budget  
* Notes  
* Friend emails

Form rules:

* Forms should feel lightweight and approachable.  
* Use helper text when the input affects the group planning flow.  
* Keep placeholders simple and specific.  
* Use error messages that explain how to fix the issue.

---

## **5\. Core UI Elements for this Product**

**Trip Dashboard**  
The trip dashboard should feel like the group’s shared planning home base.  
It should include:

* Trip name and destination  
* Travel dates or date options  
* Group members  
* Planning sections such as itinerary, availability, expenses, and decisions  
* Clear next steps for what the group still needs to do

Visual style:

* Clean card-based layout  
* Soft green background  
* White content surfaces  
* Clear primary action at the top or center of the page

**Destination and Activity Cards**  
Card contains:

* Destination or activity image  
* Name of the place or activity  
* Short description or context  
* Vote or selection controls  
* Group response summary when available

Voting options should feel simple and human, such as:

* Yes  
* Maybe  
* Not for me

Cards can animate slightly when a user votes, but motion should stay subtle and polished.  
**Group Calendar / Availability**  
Visual style:

* Clear date blocks  
* Soft green for available dates  
* Yellow for tentative dates  
* Red for conflicts or unavailable dates  
* Simple overlap indicators so users can quickly see the best shared options

The calendar should help the group answer one question quickly: “When can most people go?”  
**Itinerary**  
Itinerary items should be easy to scan and reorder.  
Each item may include:

* Time or day  
* Activity name  
* Location  
* Notes  
* Cost or reservation details when relevant

Visual style:

* Timeline or stacked card layout  
* Minimal dividers  
* Clear day groupings  
* Soft highlights for confirmed items

**Expenses**  
Expense tracking should feel practical and lightweight.  
Each expense item may include:

* Expense name  
* Amount  
* Person who paid  
* People included  
* Split status

Visual style:

* Clean table or card layout  
* Green for settled items  
* Yellow for pending balances  
* Red only for overdue or unresolved issues

---

## **6\. Imagery & Icons**

Icon style: Rounded line icons, preferably Lucide or a similar clean icon set.

Photography and illustration style:

* Warm travel imagery  
* Friends planning or traveling together  
* Maps, paths, pins, luggage, airplanes, calendars, and group moments  
* Natural, candid visuals rather than overly polished stock photos

What to avoid:

* Corporate business travel imagery  
* Generic travel agency photos  
* Overly staged friend groups  
* Dark, heavy, or cluttered visuals  
* Icons with inconsistent stroke widths or styles

Imagery should support the feeling that Tripable is for real groups making real plans together.

---

## **Implementation Notes**

* CSS framework: Tailwind  
* Deployment: Vercel  
* Design approach: web-first and easy to scan  
* Use reusable components for cards, buttons, forms, trip sections, and voting states  
* Keep spacing consistent across pages so the product feels polished

**Visual Inspiration**

* Airbnb → warm, travel-friendly experience  
* Splitwise → clear group expense handling  
* Doodle / When2Meet → simple group availability coordination  
* Notion → clean card-based organization  
* Locket → lightweight social feel

Goal: Airbnb warmth × Splitwise clarity × Doodle coordination, designed specifically for group trips.