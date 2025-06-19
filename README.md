### 모델 다운로드 ###
64x64 classifier : [https://openaipublic.blob.core.windows.net/diffusion/jul-2021/64x64_classifier.pt]                    
64x64 diffusion : [https://openaipublic.blob.core.windows.net/diffusion/jul-2021/64x64_diffusion.pt]                   

- 모델 저장 경로 : guided-diffusion/models/

### 실행 코드 ###
```Python
python scripts/classifier_sample.py --attention_resolutions 32,16,8 --class_cond True --diffusion_steps 1000 --dropout 0.1 --image_size 64 --learn_sigma True --noise_schedule cosine --num_channels 192 --num_head_channels 64 --num_res_blocks 3 --resblock_updown True --use_new_attention_order True --use_fp16 True --use_scale_shift_norm True --classifier_scale 1.0 --classifier_path models/64x64_classifier.pt --classifier_depth 4 --model_path models/64x64_diffusion.pt --batch_size 4 --num_samples 100 --timestep_respacing 250
```

