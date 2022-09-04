# Header-only Text ANSI Colorization

### Usage
```c++
static void test() {
    std::string str{"Hello World !!!"};
    std::cout << AnsiColor::colorize<AnsiColor::YELLOW>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::RED>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::GREEN>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::BLUE>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::MAGENTA>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::CYAN>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::WHITE>(str) << "\n";

    std::cout << AnsiColor::colorize<AnsiColor::YELLOW, RED>(str, true) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::RED, GREEN>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::GREEN, MAGENTA>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::BLUE, CYAN>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::MAGENTA, WHITE>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::CYAN, BLUE>(str) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::WHITE, BLACK>(str) << "\n";

    std::cout << AnsiColor::colorize<AnsiColor::YELLOW, RED>(str, true, true) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::RED, GREEN>(str, false, true, true) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::GREEN, MAGENTA>(str, true, false, true) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::BLUE, CYAN>(str, true, true, false) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::MAGENTA, WHITE>(str, false, false, true) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::CYAN, BLUE>(str, true, false, true) << "\n";
    std::cout << AnsiColor::colorize<AnsiColor::WHITE, BLACK>(str, true, true, true) << "\n";
}
```

### Test
```shell
g++ -std=c++17 -o main test/main.cc && ./main && rm ./main
```