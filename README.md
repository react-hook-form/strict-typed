<div align="center">
  #### 👷🏻‍♂️ under construction
</div>

<div align="center">
    <p align="center">
        <a href="https://react-hook-form.com" title="React Hook Form - Simple React forms validation">
            <img src="https://raw.githubusercontent.com/bluebill1049/react-hook-form/master/website/logo.png" alt="React Hook Form Logo - React hook custom hook for form validation" width="300px" />
        </a>
    </p>
</div>

<p align="center">Performant, flexible and extensible forms with easy to use validation.</p>

## Goal

React Hook Form strictly typed Field component.

## Install

    $ npm install @hookform/typed-field
    
## Quickstart    

```tsx
import { useForm } from "react-hook-form";
import { createTypedField } from "@hookform/typed-field";

type FormValues = {
  test: string;
  nested: {
    test: string;
  }[];
};

export default function App() {
  const { control, handleSubmit } = useForm<FormValues>();
  const TypedField = createTypedField<FormValues>({ control });
  const onSubmit = handleSubmit((data) => alert(JSON.stringify(data)));

  return (
    <form onSubmit={onSubmit}>
      <TypedField as="input" name="test" rules={{ required: true }} />
      <TypedField
        as="input"
        name={["nested", 0, "test"]}
        rules={{ required: true }}
      />
      <input type="submit" />
    </form>
  );
}
```

## Backers

Thanks goes to all our backers! [[Become a backer](https://opencollective.com/react-hook-form#backer)].

<a href="https://opencollective.com/react-hook-form#backers">
    <img src="https://opencollective.com/react-hook-form/backers.svg?width=950" />
</a>

## Organizations

Thanks goes to these wonderful organizations! [[Contribute](https://opencollective.com/react-hook-form/contribute)].

<a href="https://github.com/react-hook-form/react-hook-form/graphs/contributors">
    <img src="https://opencollective.com/react-hook-form/organizations.svg?width=950" />
</a>

## Contributors

Thanks goes to these wonderful people! [[Become a contributor](CONTRIBUTING.md)].

<a href="https://github.com/react-hook-form/react-hook-form/graphs/contributors">
    <img src="https://opencollective.com/react-hook-form/contributors.svg?width=950" />
</a>
