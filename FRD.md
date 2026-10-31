# Functional Requirements Document (FRD)

**Project:** Lumina Atelier: AI Virtual Wardrobe Stylist

This FRD describes how the app meets the requirements in the [BRD](BRD.md).

## 1. Document control

| Item | Detail |
|---|---|
| Project | Lumina Atelier: AI Virtual Wardrobe Stylist |
| Team | Neha Somawanshi, Trupti Holkar, Samiksha Khatawkar |
| Platform | Web app built in Google AI Studio |
| Data | Unsplash images and a Heritage Collection dataset |
| Related document | [BRD](BRD.md) |

## 2. System flow

```
Capture / Upload Image
        |
Image Preprocessing      (resize, background removal, noise reduction)
        |
Feature Extraction       (body shape, colour analysis, texture identification)
        |
Outfit Recommendation    (match features with the database, suggest outfits)
        |
Virtual Try-On & Display (overlay the outfit and show the final image)
```

## 3. Functional requirements

### 3.1 Photo input

| ID | Requirement | BR |
|---|---|---|
| FR-1 | Let the user upload an image with **Import Piece** | BR-1 |
| FR-2 | Let the user take a photo with the live camera using **Open Lens** | BR-1 |

### 3.2 Image analysis

| ID | Requirement | BR |
|---|---|---|
| FR-3 | Preprocess the image: resize, background removal and noise reduction | BR-3 |
| FR-4 | Extract features: body shape detection, colour analysis and texture identification | BR-3 |
| FR-5 | Match the features with the archive and generate suitable outfit suggestions | BR-4 |

### 3.3 Archive and browsing

| ID | Requirement | BR |
|---|---|---|
| FR-6 | Offer a choice of Women's Wear (121 pieces) or Men's Wear (91 pieces) in the **Atelier Archive** | BR-2 |
| FR-7 | Organise pieces into Tops, Bottoms, Dresses, Footwear and Accessories | BR-2 |
| FR-8 | Let users filter by category and by dataset source | BR-2, BR-10 |
| FR-9 | Provide search by silhouette, texture or category, including voice search | BR-9 |
| FR-10 | Let users add, edit and delete pieces in the archive | BR-10 |

### 3.4 Virtual try-on

| ID | Requirement | BR |
|---|---|---|
| FR-11 | Let users select a top, pant, sunglasses or other accessory | BR-2, BR-6 |
| FR-12 | On clicking **Invoke**, generate an image of the user wearing the selected outfit in the **Neural Mirror** | BR-6 |
| FR-13 | Accept an occasion prompt (**Manifestation Intent**) such as "A rainy morning in Milan", a wedding, a party or a casual day | BR-5 |
| FR-14 | Offer **Fabric** options such as silk, denim, cashmere, linen, velvet and leather | BR-7 |
| FR-15 | Offer **Fit** options such as slim, oversized, tailored and cropped | BR-7 |
| FR-16 | Offer **Aesthetic** options such as old money, minimalism, streetwear and boho-chic | BR-7 |

### 3.5 Outfit management and interface

| ID | Requirement | BR |
|---|---|---|
| FR-17 | **Curated Ensemble:** collect the selected pieces into one outfit | BR-8 |
| FR-18 | **Memoirs:** keep a history of past looks | BR-8 |
| FR-19 | Provide light and dark themes | BR-11 |

## 4. Screens

| Screen | Purpose | Related requirements |
|---|---|---|
| The Atelier Archive | Choose Women's or Men's category | FR-6 |
| Men's Collection | Filter by tops, bottoms, footwear and accessories | FR-7, FR-8 |
| Women's Collection | Browse the women's range, including dresses | FR-7, FR-8 |
| Neural Mirror | Upload or open the camera, add a prompt and refinements, and invoke the try-on | FR-1, FR-2, FR-12 to FR-16 |
| Try-on results | View the generated outfit image | FR-12 |

## 5. Data requirements

| ID | Requirement |
|---|---|
| DR-1 | The archive holds 121 women's and 91 men's pieces, each with an image and a category |
| DR-2 | Each piece records its dataset source (Unsplash or Heritage Collection) so users can filter by it |
| DR-3 | The user's photo is the input for analysis and try-on |
| DR-4 | Saved looks are stored so they can appear in Memoirs |

## 6. Non-functional requirements

| ID | Requirement |
|---|---|
| NFR-1 | The app must be easy to use for people without technical knowledge |
| NFR-2 | The interface must work in both light and dark themes |
| NFR-3 | The app runs from the live demo link without installation |
| NFR-4 | Image sources must be credited and used for academic purposes only |

## 7. Validation checks

| ID | Check | Expected result |
|---|---|---|
| T-1 | Open the Atelier Archive | Women's Wear and Men's Wear choices appear |
| T-2 | Count pieces in each collection | 121 women's and 91 men's |
| T-3 | Upload a photo and select a top, then click **Invoke** | An image of the user wearing the top is generated |
| T-4 | Use **Open Lens** and select sunglasses, then click **Invoke** | An image of the user wearing the sunglasses is generated |
| T-5 | Add the prompt "A rainy morning in Milan" and invoke | The look reflects the prompt |
| T-6 | Change the fabric, fit and aesthetic and invoke | The generated look changes to match the options |
| T-7 | Add pieces to the Curated Ensemble | The pieces appear together as one outfit |
| T-8 | Open Memoirs after generating a look | The past look is listed |
| T-9 | Search by a category and by voice | Matching pieces are shown |
| T-10 | Add, edit and delete a piece | The archive updates |

## 8. Known limitations

- Analysis is not real-time; real-time body and outfit analysis is future scope.
- There is no shopping link yet; e-commerce integration is future scope.
- The archive has 212 pieces, so choices are limited.
- The try-on is an AI-generated preview and may not match the real fit exactly.

## 9. Traceability

| Business requirement | Functional requirements |
|---|---|
| BR-1 | FR-1, FR-2 |
| BR-2 | FR-6, FR-7, FR-8, FR-11 |
| BR-3 | FR-3, FR-4 |
| BR-4 | FR-5 |
| BR-5 | FR-13 |
| BR-6 | FR-11, FR-12 |
| BR-7 | FR-14, FR-15, FR-16 |
| BR-8 | FR-17, FR-18 |
| BR-9 | FR-9 |
| BR-10 | FR-8, FR-10 |
| BR-11 | FR-19 |

---

Back to the [project README](README.md) or the [BRD](BRD.md).
