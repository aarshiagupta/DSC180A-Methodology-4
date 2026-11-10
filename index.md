## Aarshia Gupta

[aag022@ucsd.edu](mailto:aag022@ucsd.edu)

**Section:** D11, Property Intelligence (Cotality)
**Mentor:** Lawrence Vulis

---

**1. What is the most interesting topic covered in your domain this quarter?**

For me it was how easy it is for building data to be wrong without anyone noticing. In Pollack et al. (2025), the national structure dataset overestimated flood damage in Philadelphia by about 21%, but the totals still looked reasonable. You only saw the problem when you checked building by building. I ran into smaller versions of this myself. In DuckDB, using the wrong coordinate system doesn't give you an error, it just gives you wrong numbers. And when I traced buildings in San Diego for our OSM mapping homework, the suggested outlines sometimes followed the roof instead of the base, skipped garages, or showed the same building twice. Seeing these mistakes up close made the problem feel a lot more real than just reading about it.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

The direction I'm most excited about is checking how consistent different sources are about the same buildings. OpenStreetMap, Overture, and Microsoft all have building footprints, and the National Structure Inventory (NSI) has property records as points. When they describe the same building, how often do they disagree, and can we tell which one is right? We could link records to footprints and flag things that don't fit, like a record with no building under it, several records on one footprint, or a building type that doesn't match the footprint's size. This was one of the ideas we sent our mentor, and he mentioned that the winter work will be very similar to it, so it's the direction we're hoping to build toward.

From our meetings, our understanding is that Q2 will also involve pulling satellite imagery, extracting footprints with a foundation model (Clay), and comparing them against older footprints. That fits really well with the idea above, since freshly extracted footprints become one more source to compare. The question I'd love to answer there is whether a disagreement means something actually changed (a building was torn down or two were merged) or whether it's just a difference in how the footprint was drawn, since extraction tools changed a lot between 2021 and 2025. None of this is confirmed yet, but these are the ideas we're excited about.

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

Q1 has been a crash course in GIS: DuckDB spatial SQL, Overture Maps, editing OSM, reading papers on building data and risk, and analyzing OSM footprints for four San Diego zip codes (mine is 92103). We've also set up our repo and drafted the intro and data sections of our report. Looking back, I'd anchor all of this to a research question earlier, so each homework builds toward one analysis.

I'd also set up ground truth from the start. Last year's Cotality team had trouble checking their results because they didn't have any. Since Cotality can't share its data with us, a small set of buildings we've traced or checked by hand in our zip codes would give us something reliable to test against, and the errors we saw while mapping would be a great place to start.

**4. What other techniques would you be interested in using in your project?**

I'd like to try different ways of measuring how much two outlines of the same building differ, like how much they overlap or how far apart their centers are. Since we won't have many labeled errors, unsupervised anomaly detection could help flag buildings that look unusual. Comparing a building to its neighbors also seems useful, since a footprint that looks very different from the ones around it is more likely to be wrong. Adding errors on purpose (shifting, shrinking, or merging buildings) would let us measure how well these methods actually work. And I'm really looking forward to working with the Clay model if we use imagery.

---

**Is our domain on track for Quarter 1, and what is feasible for Quarter 2?**

We've made progress, even if things aren't fully settled. We've finished the homeworks and mapping work, set up our repo, pulled OSM footprints for our zip codes, and drafted parts of our report.

Early on, we weren't sure what our concrete Q1 project should be, since Q1 was set up as more of a learning quarter. So we talked to our TA about it, then brainstormed a set of project ideas based on what we'd learned and shared them with both our mentor and our TA. That got us some clarity in the right direction: our mentor said the winter work will be very similar to our cross-source consistency idea. We don't have 100% clarity yet, and a few details from our meetings still need confirming.

For Q2, we're hopeful we'll get to build out the cross-source consistency idea: linking NSI records to footprints from OSM, Overture, and Microsoft, flagging where they disagree, and eventually adding Clay-extracted footprints as another source. We've also let our mentor know that we're excited to take on challenging work and would like a project that really pushes us.
