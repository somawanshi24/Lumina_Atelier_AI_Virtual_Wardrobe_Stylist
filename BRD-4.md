# Business Requirements Document (BRD)

**Project:** Lumina Atelier: AI Virtual Wardrobe Stylist

This BRD was written for the use case described in the README. The stakeholder roles other than the project team are fictional. For the detailed functional specification, see the [FRD](FRD.md).

## 1. Document control

| Item | Detail |
|---|---|
| Project | Lumina Atelier: AI Virtual Wardrobe Stylist |
| Project type | Academic team project, B.Tech ENTC (Group A01) |
| Team | Neha Somawanshi, Trupti Holkar, Samiksha Khatawkar |
| Guide | Dr. Sandeep Kadam |
| Built with | Google AI Studio (AI-assisted development) |
| Status | Delivered; research presented at ICA6NT 2026 |

## 2. Purpose and scope

**Purpose.** Help people see how an outfit looks on them before choosing or buying it, by combining outfit recommendation and virtual try-on in one easy-to-use app.

**In scope**
- A curated fashion archive for women's wear (121 pieces) and men's wear (91 pieces)
- Photo input by upload or live camera
- Image preprocessing and feature extraction (body shape, colour, texture)
- Outfit recommendation from the user's features and a text prompt
- Virtual try-on that generates an image of the user wearing the selected pieces
- Refinement by fabric, fit and aesthetic
- Outfit collection, history of past looks, search and archive management

**Out of scope (future scope)**
- Real-time body and outfit analysis
- E-commerce integration to buy the pieces tried on
- Larger and more diverse clothing datasets

## 3. Stakeholders

| Stakeholder | Role | Interest |
|---|---|---|
| Shoppers and everyday users | Primary users | See how a piece looks on them and get outfit ideas for an occasion |
| Fashion retailers (fictional) | Potential beneficiaries | Fewer purchases that customers regret, and a more engaging experience |
| Project guide and conference reviewers | Reviewers | A well-researched, well-documented design |
| Project team | Builders | A working, easy-to-use app |

## 4. Business problem and objectives

Choosing an outfit that suits you is hard, and online shoppers cannot see how a piece will look on them before buying. Existing smart-mirror and stylist systems often lack fashion focus, clothing analysis or real-time results.

| ID | Objective | Success measure |
|---|---|---|
| BO-1 | Suggest outfits from user-uploaded photos | Recommendations produced from the user's photo |
| BO-2 | Analyse the user's body features and appearance | Body shape, colour and texture identified from the image |
| BO-3 | Recommend outfits from user prompts such as a wedding, party or casual day | Prompt changes the look that is generated |
| BO-4 | Show a virtual try-on preview | An image of the user wearing the selected outfit |
| BO-5 | Deliver a personalised, intelligent styling experience | Fabric, fit and aesthetic refinements, plus saved looks |

## 5. Business requirements

| ID | Requirement | Objective | Priority |
|---|---|---|---|
| BR-1 | Users can provide their photo by upload or by live camera | BO-1 | Must |
| BR-2 | Users can browse a curated fashion archive by gender and category | BO-4 | Must |
| BR-3 | The system analyses the photo to find body shape, colour and texture | BO-2 | Must |
| BR-4 | The system recommends outfits that match the user's features | BO-1, BO-2 | Must |
| BR-5 | Users can describe an occasion in a text prompt to guide the look | BO-3 | Must |
| BR-6 | Users can generate a try-on image of themselves wearing selected pieces | BO-4 | Must |
| BR-7 | Users can refine the look by fabric, fit and aesthetic | BO-5 | Should |
| BR-8 | Users can collect pieces into one outfit and review past looks | BO-5 | Should |
| BR-9 | Users can search the archive, including by voice | BO-5 | Should |
| BR-10 | Admins can add, edit and delete pieces in the archive | BO-5 | Should |
| BR-11 | The app supports light and dark themes | BO-5 | Could |

## 6. Assumptions and constraints

- The project was built with the help of Google AI Studio, and the demo runs there.
- Fashion images come from Unsplash and a Heritage Collection dataset, and belong to their respective owners.
- It is an academic project, not a commercial product.
- The try-on is a generated image, so it shows an approximation of how the outfit looks.
- Real-time analysis and shopping are future scope.

## 7. Risks

| Risk | Impact | Response |
|---|---|---|
| Generated try-on images may not match the real fit | Users may misjudge how a piece looks | Present the output as a preview; improve with larger datasets |
| Users upload personal photos or use the camera | Privacy concern | The README does not describe photo handling; clearly stating how photos are used is recommended |
| Images belong to third parties | Copyright concern | Credit sources in the README; the project is for academic use |
| Dependence on Google AI Studio | The demo may change or become unavailable | Keep screenshots and documentation in the repository |
| Limited archive size (212 pieces) | Fewer outfit options | Larger and more diverse datasets listed as future scope |

## 8. Acceptance criteria

- A user can upload a photo or use the camera and select pieces from the archive.
- Clicking **Invoke** produces an image of the user wearing the selected outfit.
- A prompt such as "A rainy morning in Milan" and the fabric, fit and aesthetic options change the result.
- The archive shows 121 women's pieces and 91 men's pieces across the listed categories.
- Users can save outfits, view past looks, search and manage archive items.

---

Back to the [project README](README.md).
