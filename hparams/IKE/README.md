alg_name: "IKE"
model_name: "./hugging_cache/llama-2-7b"
sentence_model_name: "./hugging_cache/all-MiniLM-L6-v2"
device: 0
results_dir: "./results"

k: 32 
#the number of demonstration

## Multimodal
- `task_name`: Specifies the task name, like `vqa` or `caption`.

- `qformer_checkpoint`: Specifies the checkpoint file for QFormer used in the model. Example: `hugging_cache/blip2_pretrained_flant5xxl.pth`.

- `qformer_name_or_path`: Provides the name or path of the pre-trained QFormer model. This could be a name of a pre-trained model from the model hub or a local path to the model. Example: `bert-base-uncased` or `./local/path/to/model`.

- `state_dict_file`: Specifies the checkpoint file for the Vision Transformer (ViT) used as the vision encoder. Example: `hugging_cache/eva_vit_g.pth`.

## image
- `coco_image`:  The directory storing the COCO dataset. We can access specific images by appending the image path to this directory, like `coco_image + "val2014/COCO_val2014_000000451435.jpg"`.
- `rephrase_image`: The directory storing rephrase images generated by the diffusion model based on COCO. Specific images can be accessed by appending the image path to this directory, like `rephrase_image + "val2014_image_rephrase/451435003_COCO_val2014_000000451435.png"`