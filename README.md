# Ansible Playbook: Hamurabi

This project is an attempt to bring the text-based strategy game [Hamurabi](https://en.wikipedia.org/wiki/Hamurabi_(video_game)) to Ansible.
I intend to stay close to the BASIC version from [David H. Ahl](https://en.wikipedia.org/wiki/David_H._Ahl) while also incorporating a few niceties to improve user experience.

The goal is to govern the Ancient Sumeria for a duration of 10 years, managing your grain between feeding your people, planting new crops, buying or selling land.
Rats can randomly come and eat your stock of grains while plague can decimate your population.
Be careful in your calculations!

The game ends if:

- 10 years passed.
- 45% of the population died of starvation during one year

A successful play is measured by the ratio of owned land compared to the population: more than seven acres of land per people is a win.

## How to play

The following packages are necessary:

- ansible

Simply run the following command:

```sh
$ ansible-playbook hamurabi.yml
...
```

## Testing

Note: testing requires `molecule` as an additional dependency.

There is only one testing scenario right now, which tests player actions and their limits such as trying to sell too much land, planting crops without enough seeds, etc.

To run it:

```sh
$ molecule converge
...
```

## TODO

Here is a list of features yet to be implemented:

- Count the number of poor souls who starved due to the player negligence.
- Implement a system to provide a seed to improve testing.

## Caveats

Ansible is not exactly a comfortable medium to play video games.
Consider yourself warned.

## License

ISC

## Contributing

Either send [send GitHub pull requests](https://github.com/tleguern/ansible-playbook-hamurabi) or [send patches on SourceHut](https://lists.sr.ht/~tleguern/misc).

## Author Information

Tristan Le Guern <tleguern@bouledef.eu>
