# 李弘毅 Machine Learing 2023 Spring 作業 

1. Regression
    + Private 0.9123 / Public 0.86817 Strong baseline
        #### 觀察相關係數 
        #### 爆調參數

2. Classification

    Leaderboad

    + Private 0.75128 / Public 0.75001 Strong baseline
        #### Sample code layer 較小 dim 較大
        #### 輕微overfit
    + Private 0.70358 / Public 0.70321 Medium baseline
        #### Transformer Encoder
        #### 嚴重overfit
    + Private 0.70358 / Public 0.70321 Medium baseline
        #### Ensemble + Transformer & Sample
        #### overfit 效果不佳
    + Private 0.76065 / Public 0.76114 Strong baseline
        #### Ensemble + Sample Code
        #### overfit
        #### label smooth

    可以改善地方

    + 降低batch size 


3. CNN

    + Private 0.80333 / Public 0.814 Medium baseline
        #### efficientnet_v2_m
        #### TTA 
        #### 很多Data Augmentation 
        #### Label Smooth
        #### train/valid資料比例重新分配
        #### 輕微overfit
    
    + Private 0.80333 / Public 0.814 Strong baseline
        #### resnext101_32x8d
        #### 調整Data Augmentation
        #### Label Smooth
        #### train/valid資料比例重新分配
        #### 輕微overfit

     可以改善地方

    + Data Augmentation好像做太多?
    + train / valid資料重新分配的地方不能有隨機性 or 用 random seed控制

4. Self-attention
    + Private 0.94175 / Public 0.936 boss baseline
        #### TransformerEncoder
        #### 調整參數
        #### Train超久
        #### 超乎想像的好
        #### 嚴重overfit
    + Private 0.9295 / Public 0.92625 boss baseline
        #### Comformer
        #### 調整參數
        #### 超乎想像的好
        #### 輕微overfit
        
    + Private 0.96425 / Public 0.9635 boss baseline
        #### Comformer + Attention pooling layer
        #### overfit
        #### 減少predict layer
        

5. Transformer
    
    只有修課學生可以交QQ

    + loss 3.8388
        #### Sample Code RNN +  lr scheduling
    + loss ?
        #### Sample Code Transformer

6. Generative Model

    + DDPM

    + DCGAN

    + WGAN

    + WGAN-GP

    + StyleGAN