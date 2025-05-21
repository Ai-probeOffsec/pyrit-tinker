<p align="center"><img src="./doc/roakey.png" width="150"></p>

# Python Risk Identification Tool for generative AI (PyRIT)

The Python Risk Identification Tool for generative AI (PyRIT) is an open source
framework built to empower security professionals and engineers to proactively
identify risks in generative AI systems.

pyrit-tinker is an enhanced fork of Microsoft's [PyRIT (Python Risk Identification Tool for LLMs)](https://github.com/microsoft/pyrit) framework, specifically designed to integrate with Burp Suite for automated AI security testing.

- Check out our [website](https://azure.github.io/PyRIT/) for more information
  about how to use, install, or contribute to PyRIT.
- Visit our [Discord server](https://discord.gg/FsN225wC) to chat with the team and community.

## Trademarks

This project may contain trademarks or logos for projects, products, or services.
Authorized use of Microsoft trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must
not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's
policies.

## Citing PyRIT

If you use PyRIT in your research, please cite our preprint paper as follows:

```
@misc{munoz2024pyritframeworksecurityrisk,
      title={PyRIT: A Framework for Security Risk Identification and Red Teaming in Generative AI Systems},
      author={Gary D. Lopez Munoz and Amanda J. Minnich and Roman Lutz and Richard Lundeen and Raja Sekhar Rao Dheekonda and Nina Chikanov and Bolor-Erdene Jagdagdorj and Martin Pouliot and Shiven Chawla and Whitney Maxwell and Blake Bullwinkel and Katherine Pratt and Joris de Gruyter and Charlotte Siska and Pete Bryan and Tori Westerhoff and Chang Kawaguchi and Christian Seifert and Ram Shankar Siva Kumar and Yonatan Zunger},
      year={2024},
      eprint={2410.02828},
      archivePrefix={arXiv},
      primaryClass={cs.CR},
      url={https://arxiv.org/abs/2410.02828},
}
```

Additionally, please cite the tool itself following the `CITATION.cff` file in the root of this repository.

# PyRIT Gandalf Challenge

This repository contains code for running the Gandalf Challenge using PyRIT (Python Risk Identification Tool). The implementation uses the PAIR (Prompt Automatic Iterative Refinement) orchestrator to attempt the challenge.

## Prerequisites

- Python 3.8+
- PyRIT library
- OpenAI API access

## Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/pyrit-gandalf-challenge.git
cd pyrit-gandalf-challenge
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install pyrit
```

4. Create a `.env` file in the root directory with your API keys:
```
OPENAI_API_KEY=your_api_key_here
```

## Usage

Run the Gandalf challenge:
```bash
python gandalf_pair_attack.py
```

## Configuration

- The default Gandalf level is set to LEVEL_8
- PAIR orchestrator parameters can be adjusted in the script:
  - depth: Number of iterations
  - objective_achieved_score_threshold: Success threshold
  - desired_response_prefix: Expected response prefix

## Note

Make sure to never commit your `.env` file or any files containing API keys to the repository. These files are already included in `.gitignore`.
"# pyrit-tinker" 
