# Извлечение признаков с помощью RBM

Сравнение трёх способов представления рукописных цифр MNIST 28×28 при одном классификаторе - Logistic Regression:

- исходные 784 пикселя;
- PCA, 256 главных компонент;
- RBM, 256 скрытых признаков.

## Результаты

| Признаки | Accuracy | Macro-F1 |
| --- | ---: | ---: |
| Пиксели | 92,55% | 0,9244 |
| PCA | 92,53% | 0,9242 |
| RBM | **96,14%** | **0,9610** |

Результаты были получены на одном запуске с `seed=42` и приведены для тестовой выборки из 10 000 изображений.

## Файлы

- [`RBM_MNIST.ipynb`](RBM_MNIST.ipynb) — код эксперимента и графики;
- [`RBM_MNIST_presentation.pptx`](RBM_MNIST_presentation.pptx) — презентация для доклада.

## Данные и материалы

- [MNIST](https://storage.googleapis.com/tensorflow/tf-keras-datasets/mnist.npz)
- [Описание BernoulliRBM в scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.neural_network.BernoulliRBM.html)

Ноутбук содержит реализацию RBM на PyTorch с обучением CD-1 и не использует `BernoulliRBM` из scikit-learn.
