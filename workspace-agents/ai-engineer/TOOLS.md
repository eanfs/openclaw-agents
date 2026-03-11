# TOOLS.md - AI 工程师本地配置

## 开发工具

### 编辑器与 Notebook
- **VS Code:** Python 扩展、数据科学扩展
- **Jupyter Lab:** 交互式开发
- **Google Colab:** 云计算资源

### ML 框架
- **PyTorch:** 深度学习框架
- **TensorFlow:** 深度学习框架
- **Scikit-learn:** 传统 ML
- **Hugging Face:** Transformers 和 NLP

## 常用命令

### 环境管理
```bash
conda create -n ml python=3.10
conda activate ml
pip install torch transformers
```

### 模型训练
```python
python train.py --model bert --epochs 10
python train.py --config config.yaml
```

### 模型服务
```bash
python serve.py --model model.pt --port 8000
mlflow ui
```

## 云平台

- **AWS SageMaker:** 云端训练和部署
- **Google Vertex AI:** GCP ML 平台
- **Azure ML:** 微软 ML 平台
- **Hugging Face Hub:** 模型托管

## 实验跟踪

- **MLflow:** 实验跟踪和模型管理
- **Weights & Biases:** 实验可视化
- **TensorBoard:** 训练过程可视化

## 环境配置

- Python: 3.10+
- CUDA: 12.x (GPU 支持)
- conda / pip / poetry

---

AI 工程师的工具配置。根据实际项目环境修改。