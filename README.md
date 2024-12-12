EA-PS: Estimated Attack Effectiveness based Poisoning Defense in Federated Learning under Parameter Constraint

------------------------------------------------------------------------------------------------------------------------------------------------------------
This repository contains the code for the paper "LeadFL: Client Self-Defense against  Model Poisoning in Federated Learning"& other baseline methods as follows
https://github.com/CarlosChu-c/LeadFL.
https://github.com/JMGaljaard/fltk-testbed
https://github.com/jeremy313/FL-WBC
https://github.com/sparsefed/sparsefed
https://github.com/ebagdasa/backdoors101


## Abstract
Federated learning is vulnerable to targeted model poisoning backdoor attacks due to the characteristics of its learning paradigm. There are a number of server-based and client-based backdoor defense methods to alleviate the impact caused by the attacks. However,  when facing powerful adversarial attacks with high variance, the defensive methods fail to guarantee robust and stable performance. 

In this paper, we propose a client-side defense method, \texttt{EA-SP}, which can be effectively combined with server-side methods to address the above issues. The key idea of \texttt{EA-SP} is to constrain the perturbation range of local parameters while minimizing the impact of attacks. We transform the client-side defense problem through optimization and linear robust optimization methods. Meanwhile, we prove that the objective function for minimizing the impact of attacks has a smaller upper bound, and under the constraint of local parameter perturbation, it has a smaller coverage radius and a larger certified radius to ensure the performance and robustness of \texttt{EA-PS}. Experimental results show that, compared with other client-side defense methods, \texttt{EA-PS} can be combined with different server-side defense methods under both i.i.d. and non-i.i.d. data distributions, achieving lower attack success rates and more stable defense performance with smaller variance. 

## Requirements
Requirements are listed in `requirements.txt`. To install them, run `pip install -r requirements.txt`.

## Quick Start
```
python3 -m fltk single ./configs/temlate.yaml
```
In the template, the client-side defense is `LeadFL`, the server-side defense is `Bulyan`, the attack is 9-pixel pattern backdoor attacks,and the dataset is `FashionMNIST`. You can change the parameters in the template to run other experiments.
