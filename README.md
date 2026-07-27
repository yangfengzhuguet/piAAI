# piAAI：A protein interaction-aware framework for antibody-antigen interaction prediction
Antibody–antigen interaction (AAI), a highly specific type of protein–protein interaction (PPI), plays a critical role in therapeutic antibody development and vaccine design. However, protein language models (pLMs) trained on single-chain protein sequences are suboptimal for AAI tasks. Here, we present piAAI, a protein interaction-aware framework for AAI prediction. piAAI focuses on the antibody complementarity-determining regions (CDRs) and framework regions (FRs), and learns antibody–antigen interaction information by quantifying differences in amino acid (AA) physicochemical properties between CDR (or FR) sequences and antigen sequences. The results demonstrate that piAAI outperformed existing computational methods across multiple AAI-related tasks, including binding, neutralization effects, half-maximal inhibitory concentration (IC50), and affinity prediction. Under data-scarce conditions, piAAI can still learn target virus-specific AAI patterns with limited supervised samples. In addition, we found that antibody heavy-chain CDR3 (CDR-H3) exhibits high length diversity and unique AA positional distribution compared with other CDRs. Specifically, the flanking positions of CDR-H3 are relatively conserved and enriched with opposite-charge amino acids, aspartic acid (D) and arginine (R), respectively. Meanwhile, piAAI can also accurately predict the disruptive effects of AA mutations on AAI. Finally, an interleukin-15 (IL-15)-targeting antibody screening experiment further validated the potential of piAAI for therapeutic antibody discovery.
![image](https://github.com/yangfengzhuguet/piAAI/blob/main/workflow.jpg)
# ProtTrans
You need to prepare the pretrained language model ProtTrans to run IKANBind:  
Download the pretrained ProtT5-XL-UniRef50 model ([guide](https://github.com/agemagician/ProtTrans)).  
# ESM-2
You need to prepare the pretrained language model ESM-2 to run IKANBind:  
Download the pretrained ESM-2 model ([guide](https://github.com/facebookresearch/esm)).  
# ESMFold
The protein structures should be predicted by ESMFold to run IKANBind:  
Download the ESMFold model ([guide](https://github.com/facebookresearch/esm))  
# Run IKANBind for prediction
Simply run:  
```
Please download the corresponding model parameters from the link (https://drive.google.com/drive/folders/1fE41iSYFBWfxkYEgjw3kzm1AAnzWJ3oyo)
Then run：
python main.py
please note：The above program loads the DNA/RNA model parameters for testing by default. If you want to retrain the model, please set the flag in main.py to train.
```
# contact
Yongxian Fan (yongxian.fan@gmail.com)  
Xiaoyong Pan (2008xypan@sjtu.edu.cn)
