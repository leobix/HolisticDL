# HolisticDL

```train_uci.py``` allows you to train an HDL feed-forward neural network.

Arguments:

- batch_range, type=int, default=[64]: help="batch sizes to train the network"

- ratio_range, type=float, default=[0.8], help="ratio between validation and test set")

parser.add_argument("--model", "-m", type=str, required=True, choices=["ff", "cnn"],
                            help="model type, either ff or cnn")

parser.add_argument("--stable", action="store_true",
                            help="stable version")

parser.add_argument("--dropout", type=float, default=1,
                            help="dropout rate, 1 is no dropout, 0 is all set to 0")

parser.add_argument("--robust", "-r", type=float, default=0,
                            help="Uncertainty set parameter for training robustness.")

parser.add_argument("--robust_test", "-rtest", type=float,  nargs='+', default=[1e-5, 1e-4, 1e-3, 1e-2, 1e-1],
                            help="Uncertainty set parameter for evaluating robustness.")

parser.add_argument("--l2", type=float, default=0,
                            help="l2 regularization rate")

parser.add_argument("--l0", type=float, default=0,
                            help="l0 regularization rate")

parser.add_argument("--reg_stability", type=float, default=0,
                            help="reg stability regularization rate")

parser.add_argument("--l1_size", type=int, default=256,
                            help="number of nodes in the first layer, 784 -> l1_size")

parser.add_argument("--l2_size", type=int, default=128,
                            help="number of nodes in the first layer, l1_size -> l2_size")

parser.add_argument("--data_set", type=str, default="mnist",
                            help="number of subsets")

parser.add_argument("--train_size", type=float, default=0.80,
                            help="training percent of the data")

parser.add_argument("--lr", type=float, default=0.001,
                            help="Adam lr")

parser.add_argument("--val_size", type=float, default=0.20,
                            help="validation percent of the data e.g., 0.25 means 0.25*traning size")
