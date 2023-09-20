# Our goal is to create a video in which a person drinking a Coke Zero is changed to a person drinking a Sprite.

## First, we will change a single image of a person drinking a Coke Zero to one of a person drinking a Sprite.

### First attempt: Using Stable Diffusion from HuggingFace.
We found HuggingFace's "runwayml/stable-diffusion-inpainting" model performed much better than the Stable Diffusion model in this library.

Masking the whole coke can produces crappy results. Masking all of it, and replacing the center with a sprite can, is much better (still not production-quality).

To run with 50 diffuser steps:
```python scripts/hf_diffuser.py --indir data/inpainting_v2/ --outdir inpainting_v2_output_hf```

Next steps:
- How/what does Adobe do in this space?
- Is there a better inpainting model we can use?
