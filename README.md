# Speed of sound prediction

> Predicting speed of sound in aqueous electrolytic solutions using machine learning.

Code and text for my 2019 computer science Bachelor thesis at MFF UK in Prague. The thesis combined my interest and expertise in both chemistry and machine learning.

## Code

The repository contains copy of thesis attachments. Read [`instructions.md`](./instructions.md) for information on repository structure and instructions for running / exploring the contents of the accompanying notebooks.

Note that the [`htmls`](./htmls/) directory contains exported notebooks including cell results, while the [`notebooks`](./notebooks/) directory contains notebooks in reset state. This is sadly a bit unfortunate for online viewing on GitHub.

The data directory is empty. However, all data for the experiments can be downloaded from sources listed in the thesis.

## Thesis

Full text is available [here](https://dspace.cuni.cz/handle/20.500.11956/108371).

### Abstract:

<cite>This bachelor thesis presents a novel approach for speed of sound prediction in aqueous electrolytic solutions using machine learning techniques. A single model capable of accurately predicting the speed of sound in selected electrolytic aqueous solutions at different temperatures and molalities is trained. The machine learning experiment is designed to exploit the dissociation of electrolytes in water. Electrolytes are viewed as cation/anion pairs. Therefore, electrolyte description is based purely on its constituting ions. This approach allows to view the available data as a matrix in which rows represent cations, columns anions and each cell a full electrolyte. The idea of being able to fill cells for which no speed of sound data is yet available is tested within the thesis. The final model’s accuracy is compared to existent research on speed of sound prediction. However, some of the model approaches are novel and have no existing comparable settings.</cite>
