# PyTorchModelHubMixin-template

a template for the PyTorchModelHubMixin

## how to use

```
pip install git+https://github.com/not-lain/PyTorchModelHubMixin-template.git
```

```python
from MyModule import MyModel # already added to src\MyModule\__init__.py

model = MyModel(a=5,b=3) # initialize the model

model.save_pretrained(local_path) # save locally

model.push_to_hub(repo_id) # push to 🤗
```

## How to load and reinitialize

```python
from MyModule import MyModel
model = MyModel.from_pretrained(path_or_repo_id) # initialize the model and inject the weights
```

## TIP 
after bilding your own library (this repo is considered a library) you can open a pull request [on this file](https://github.com/huggingface/huggingface.js/blob/main/packages/tasks/src/model-libraries.ts) to make your library semi-official on huggingface
